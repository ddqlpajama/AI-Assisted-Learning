# 🧠🤖 AI-Assisted Robotics Learning System
Welcome to the AI-assisted system designed to master robotics through Modern Robotics and ROS tutorials. This project is a long-term self-study framework, powered by multiple AI agents to accelerate understanding, documentation, and output through blog posts and structured notes.

## 🚀 Project Goals
- Master robotics through the Modern Robotics textbook and ROS-based tutorials.
- Build a self-contained robotics project by the end of 9–12 months.
- Use LLMs and automation to assist with study, note-taking, and content generation.
- Maintain reproducible, local-first tooling that respects privacy and performance.

## 🧩 System Overview
The system comprises three modular AI agents and an orchestrator:

| Agent              | Description                                                                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 🤖 Chatbot AI      | Multi-model assistant for Q\&A (uses GPT-4, Claude, or local LLMs). Includes retrieval-augmented generation (RAG), citation injection, and web search. |
| 📝 Notetaking AI   | Heuristically triggers note capture and summarization. Generates Obsidian-compatible Markdown, organized by textbook chapters or ROS module.           |
| 📢 Blog-Writing AI | Auto-generates blog posts based on study milestones. Uses a first-person narrative and emphasizes problem-solving and "aha" moments.                   |

## 📦 Tech Stack
- Language: Python
- LLMs: GPT-4, Claude, optional local LLMs via Ollama or LM Studio
- Frontend: TUI or minimal web UI (optional)
- Storage: Local markdown-based DB for notes (Obsidian-compatible)
- Scheduler/Orchestrator: Custom script (event-driven or CLI)
- External APIs: OpenAI, Claude (Anthropic), SerpAPI for web search (optional)

## 🛠️ Project Structure
```
ai-robotics-assistant/
├── orchestrator/        # Controls agent execution
├── agents/
│   ├── chatbot_ai/
│   ├── notetaker_ai/
│   └── blogwriter_ai/
├── data/
│   ├── notes/           # Obsidian-style markdown notes
│   └── source_docs/     # PDFs, scraped web data, textbook chapters
├── prompts/             # Prompt templates for each agent
├── utils/               # Common utilities (embedding, token handling, etc.)
├── tests/               # Test suite
└── README.md
```

## ⚙️ Setup Instructions
1. Clone the Repository
``` bash
git clone https://github.com/your-username/ai-robotics-assistant.git
cd ai-robotics-assistant
```
2. Install Dependencies
``` bash
pip install -r requirements.txt
```
3. Add API Keys
Create a .env file:
``` env
OPENAI_API_KEY=your_key_here
CLAUDE_API_KEY=your_key_here
SERPAPI_API_KEY=optional
```
4. Start the Orchestrator
``` bash
python orchestrator/main.py
```
## 🧠 Learning Sources
Textbook: Modern Robotics: Mechanics, Planning, and Control

Tutorials: [ROS Tutorials](http://wiki.ros.org/ROS/Tutorials), [ROS2 Docs](https://docs.ros.org/en/foxy/index.html)

The agents monitor your learning progression and respond to signals such as:
- Chapter completion
- Significant debugging milestones
- New ROS packages explored

## ✍️ Writing & Notes
- Notes are stored in `data/notes/` using Obsidian-compatible markdown.
- Blog posts are stored in `data/blog/` and mirror your study progression.
- Notes include citations, links to sources, and embedded diagrams if available.

## 🧪 Tests
Run unit tests for individual agents:

``` bash
pytest tests/
```

## 🛤️ Roadmap
 [x] Define architecture and agents
 [ ] Implement chatbot with RAG + citation support
 [ ] Create heuristic triggers for notetaker 
 [ ] Define blog milestone logic
 [ ] Add CLI/tui dashboard (optional)

## 🙌 Contributing
This is a personal project, but contributions, suggestions, or feedback are welcome! Please open an issue or discussion.

## 📄 License
GPL 3.0 License.
