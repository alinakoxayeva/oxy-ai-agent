# 🤖 Oxy AI Agent

A Slack-based AI agent built with Node.js, LangChain and OpenAI, with PostgreSQL for data storage.

> Built as a learning project while studying AI agents and Slack bot development.

![Node.js](https://img.shields.io/badge/Node.js-ES%20Modules-339933?logo=node.js&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-Bolt-4A154B?logo=slack&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-OpenAI-1C3C3C)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pg-4169E1?logo=postgresql&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue)

---

## ✨ Features

- 💬 Listens to Slack messages and replies using an LLM
- 🧠 Uses LangChain with OpenAI models to generate responses
- 🗄️ Stores data in a PostgreSQL database
- ⚡ Lightweight Express server for handling requests
- [Add your own feature here]

## 🛠️ Tech Stack

| Purpose | Technology |
|---|---|
| Runtime | Node.js (ES Modules) |
| Slack integration | `@slack/bolt`, `@slack/web-api` |
| AI / LLM | `@langchain/core`, `@langchain/openai` |
| Database | PostgreSQL (`pg`) |
| Server | Express |
| HTTP requests | Axios |
| Configuration | dotenv |

## 📋 Prerequisites

Before you start, make sure you have:

- [Node.js](https://nodejs.org/) (v18 or newer recommended)
- A [PostgreSQL](https://www.postgresql.org/) database (local or hosted)
- An [OpenAI API key](https://platform.openai.com/api-keys)
- A Slack app with a bot token and signing secret ([create one here](https://api.slack.com/apps))

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/alinakoxayeva/oxy-ai-agent.git
cd oxy-ai-agent
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key
SLACK_BOT_TOKEN=xoxb-your-slack-bot-token
SLACK_SIGNING_SECRET=your_slack_signing_secret
DATABASE_URL=postgresql://user:password@localhost:5432/your_database
```

> ⚠️ Never commit your `.env` file. Make sure it is listed in `.gitignore`.

### 4. Run the agent

```bash
# Start normally
npm start

# Start in development mode (auto-restarts on file changes)
npm run dev
```

## 📁 Project Structure

```
oxy-ai-agent/
├── index.js        # Application entry point: Slack app, server and agent logic
├── db.js           # PostgreSQL connection and database helpers
├── package.json    # Dependencies and scripts
├── LICENSE         # MIT License
└── .gitignore      # Files excluded from Git
```

## 🔄 How It Works

```
Slack message → Slack Bolt app → LangChain + OpenAI → response → Slack
                                        ↓
                                   PostgreSQL
```

1. A user sends a message to the bot in Slack.
2. The Slack Bolt app receives the event.
3. The message is passed to the LLM through LangChain.
4. Relevant data is read from or saved to PostgreSQL.
5. The generated answer is sent back to Slack.

## 📚 What I Learned

I built this project while following a tutorial and then customized it. Along the way I learned:

- How Slack apps and bots receive and respond to events
- How to call an LLM using LangChain and OpenAI
- How to connect a Node.js app to PostgreSQL
- How to manage secrets safely with environment variables

## 🙏 Credits

This project is based on the tutorial
"Build Your Own AI Agent – Full Course with OpenAI, Langchain, Render Deployment"
by [freeCodeCamp.org](https://www.freecodecamp.org/) and Code with Ania Kubów
([watch here](https://youtu.be/MnG0ugK2JAI)).

- Original repository: [kubowania/slack-ai-agent](https://github.com/kubowania/slack-ai-agent)
- The original idea and code belong to their creators. I followed the course and
  customized the project as part of my learning.

## 🗺️ Roadmap

- [ ] Add more Slack commands
- [ ] Improve the agent's memory and context handling
- [ ] Add error handling and logging
- [ ] Write tests
- [ ] Deploy to a cloud platform

## 🤝 Contributing

This is a personal learning project, but suggestions are welcome. Feel free to open an issue or submit a pull request.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

It is based on [kubowania/slack-ai-agent](https://github.com/kubowania/slack-ai-agent),
which is also released under the MIT License. The original copyright notice is
kept in the LICENSE file.

## 👩‍💻 Maintained by

**Alina Kokhayeva**
IT student at Azerbaijan State Oil and Industry University

GitHub: [@alinakoxayeva](https://github.com/alinakoxayeva)