# Demo Video Script 🎬

**Time Limit**: 3 Minutes
**Goal**: Show value, architecture, and live action.

---

## 0:00 - 0:30: The Hook (Problem & Solution)
**Visual**: Face camera or Title Slide "Qubic Sentinel".
**Audio**: 
"In the Qubic ecosystem, billions of units move in silence. The network is fast, but for the average user, it's opaque. Whales move markets, and we only find out after the price crashes.
Introducing **Qubic Sentinel**—a real-time intelligence layer that turns raw blockchain data into instant, actionable alerts for the community. Built entirely on a free stack."

## 0:30 - 1:15: The Architecture (How it Works)
**Visual**: Show the n8n Workflow (Zoom in on nodes).
**Audio**:
"We didn't just build a bot; we built an event-driven pipeline using n8n.
Here's how it works:
1. We poll the Qubic RPC for every single tick.
2. This JavaScript logic filters through thousands of transactions instantly.
3. It detects 'Whales' (over 1 Billion QUBIC) and specific interactions with the QX DEX.
4. Finally, we enrich the data with real-time USD prices from CoinGecko before dispatching it."

## 1:15 - 2:15: Live Demo (The "Wow" Moment)
**Visual**: Split screen: n8n "Executing" on left, Discord Channel on right.
**Action**: Trigger the "Manual Test" or wait for a live transaction.
**Audio**:
"Let's see it in action.
[Transaction hits]
Boom. Within seconds of the tick, our Discord lights up.
We see the amount—5 Billion QUBIC. The USD value—calculated instantly. And the risk score.
Simultaneously, this data is logged to our Google Sheet for long-term analysis."

## 2:15 - 2:45: The Dashboard (Visualization)
**Visual**: Switch to Looker Studio.
**Audio**:
"But alerts are just the start. All that data feeds into this live Looker Dashboard.
We can track Whale Volume trends, identify top holders, and monitor the health of the QX exchange.
This gives the community transparency they've never had before."

## 2:45 - 3:00: Conclusion
**Visual**: GitHub Repo / Title Slide.
**Audio**:
"Qubic Sentinel is open-source, free to host, and ready to deploy today. We're bringing light to the dark forest of blockchain data. Thank you."
