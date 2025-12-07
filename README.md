# Qubic Sentinel 🛡️

**The Watchtower of the Qubic Ecosystem.**

Qubic Sentinel is a real-time monitoring system that tracks high-value transactions ("Whales") and QX DEX activity on the Qubic blockchain. It delivers instant alerts to Discord and logs data for historical analysis, all running on a **100% free tech stack**.

![Architecture](docs/ARCHITECTURE.md)

## 🚀 Features

- **Whale Alerts**: Instant notifications for transfers > 1 Billion QUBIC.
- **QX DEX Monitoring**: Detects buy/sell orders on the Qubic Exchange.
- **Real-Time Valuation**: Converts QUBIC amounts to USD using CoinGecko.
- **Risk Scoring**: Flags suspicious or high-volume activity.
- **Zero Cost**: Runs entirely on free tiers of n8n, Google Sheets, and Discord.

---

## 🛠️ Setup Guide (Manual Steps)

To get this running, you need to perform a few one-time setup steps.

### Step 1: Google Sheets Setup 📊
1. Go to [Google Sheets](https://sheets.google.com) and create a new sheet named **"Qubic Sentinel Logs"**.
2. Rename the first tab (at the bottom) to `Sentinel_Logs`.
3. In the first row (A1:H1), add these exact headers:
   - `timestamp`
   - `tx_hash`
   - `source_id`
   - `dest_id`
   - `amount_qu`
   - `amount_usd`
   - `type`
   - `risk_score`
4. **Copy the Sheet ID** from the URL (it's the long string between `/d/` and `/edit`). You'll need this later.

### Step 2: Discord Webhook Setup 💬
1. Open your Discord Server settings.
2. Go to **Integrations** -> **Webhooks**.
3. Click **New Webhook**.
4. Name it "Qubic Sentinel" and choose a channel.
5. **Copy the Webhook URL**.

### Step 3: n8n Configuration ⚙️
1. **Import the Workflow**:
   - Open your n8n instance (Cloud or Local).
   - Click **"Add Workflow"** -> **"Import from File"**.
   - Select the `workflows/n8n_workflow_sentinel.json` file from this repository.

2. **Configure Credentials**:
   - **Discord**: Double-click the "Send Discord Alert" node. Paste your **Webhook URL** into the URL field.
   - **Google Sheets**: Double-click the "Log to Sheets" node.
     - You will need to connect a Google account. Follow n8n's prompt to sign in with Google.
     - Paste your **Sheet ID** into the "Spreadsheet ID" field.

3. **Activate**:
   - Toggle the **Active** switch to `On` (top right).
   - Save the workflow.

### Step 4: Looker Studio (Optional - Skipped) 📈
*This step is optional. If you want to visualize the data later, you can connect Looker Studio to your Google Sheet.*
1. Go to [Looker Studio](https://lookerstudio.google.com).
2. Click **Create** -> **Report**.
3. Select **Google Sheets** as the data source.
4. Choose your "Qubic Sentinel Logs" sheet.

---

## 📂 Project Structure

- `workflows/`: Contains the n8n workflow JSON file.
- `config/`: Configuration templates.
- `docs/`: Architecture and design documentation.

## 📄 License

MIT License. Free to use and modify.
