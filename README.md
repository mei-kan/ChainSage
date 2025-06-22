# 🔮 ChainSage — Your AI-Powered Web3 Intelligence Agent

ChainSage is a conversational Web3 assistant that lets anyone query real-time blockchain data using natural language. Powered by **Nodit’s Model Context Protocol (MCP)** and live multi-chain APIs, ChainSage enables developers, traders, and researchers to interact with wallets, tokens, and smart contracts through an intuitive chat interface.

Built for **Nodit Summer WaveHack ☀️🌊**, ChainSage bridges the gap between **AI and blockchain infrastructure**.

---

## 🧠 What Can ChainSage Do?

Ask questions like:
- “What tokens has Vitalik received in the past 30 days?”
- “Who are the top holders of $USDC on Ethereum?”
- “Did wallet `0x123...def` receive any NFTs this month?”
- “Notify me if a transfer of over 50 ETH happens on this wallet.”

And receive structured, real-time answers — no technical knowledge or API familiarity needed.

---

## 🔧 How It Works

ChainSage uses:
- **Nodit MCP** to dynamically call blockchain APIs via an LLM
- **Nodit Web3 Data API** to fetch balances, token transfers, and holders
- **Nodit Webhooks/Streams** to subscribe to real-time wallet activity
- A simple **chat frontend** to input natural language queries

---

## 🚀 Features

| Feature                          | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| 🧠 Natural Language Interface    | Ask questions in plain English                                             |
| ⚡ Real-time Wallet Monitoring   | Get alerts for large token transfers or contract interactions              |
| 🔗 Multi-chain Support           | Supports Ethereum and Aptos (Polygon, XRPL, etc. planned)                  |
| 📊 Wallet & Token Analytics      | View balances, token history, and top holders                              |
| 🤖 LLM + MCP Powered Agent       | AI agent interprets and executes blockchain queries with dynamic context   |

---

## 🛠️ Technologies Used

- **Frontend**: React.js + TailwindCSS
- **Backend**: Node.js / Express (for Webhook listener & routing)
- **AI Agent**: OpenAI (or any LLM) integrated with Nodit MCP
- **Nodit Services**:
  - ✅ Node API
  - ✅ Web3 Data API
  - ✅ Streams / Webhook
  - ✅ Model Context Protocol (MCP)

---

## 📂 Project Structure

```

chainsage/
├── frontend/                # Chat UI built with React
├── backend/                 # Express server for MCP + Webhooks
│   ├── routes/
│   ├── webhook-handler.js
│   └── mcp-config.json
├── mcp-server/              # Nodit MCP setup
├── prompts/                 # Example prompts & test cases
├── docs/                    # Architecture diagrams & setup docs
└── README.md

````

---

## 📥 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/chainsage.git
cd chainsage
````

### 2. Install Dependencies

```bash
cd backend
npm install
```

### 3. Configure MCP

Edit `mcp-config.json`:

```json
{
  "mcpServers": {
    "nodit": {
      "command": "npx",
      "args": ["@noditlabs/nodit-mcp-server@latest"],
      "env": {
        "NODIT_API_KEY": "YOUR_NODIT_API_KEY"
      }
    }
  }
}
```

Run the MCP server:

```bash
npm run mcp
```

### 4. Run Frontend

```bash
cd ../frontend
npm install
npm run dev
```

---

## 📌 Milestone Summary (WaveHack Submission)

> **Goal for this Wave:**
> Finalize architecture and complete MCP + Web3 API integration. Enable the agent to answer queries about token transfers and wallet balances using Nodit MCP.
> Done with the Ideation of ChainSage, and will submit a working demo in Wave 3.

---

## 🧪 Example Prompts to Try

* `"What tokens did 0xd8dA...6045 receive in May?"`
* `"Track large transactions on Ethereum above 100 ETH."`
* `"Get top 10 holders of USDT on Aptos."`

---

## 📚 Resources & Credits

* [Nodit Developer Docs](https://docs.nodit.io/)
* [Nodit MCP Docs](https://docs.nodit.io/mcp)
* [OpenAI API](https://platform.openai.com/)

---

## 🏗️ Future Plans

* [ ] Telegram Bot interface
* [ ] Support more blockchains (XRPL, Bitcoin, etc.)
* [ ] AI-driven smart contract summarizer
* [ ] Historical token analytics with graph plots

---

## 📝 License

MIT License — feel free to fork, build, and contribute.
