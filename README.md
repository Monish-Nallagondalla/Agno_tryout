# Agno Tryout

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive repository for experimenting with the [Agno](https://github.com/agno-agi/agno) framework, showcasing various AI agent implementations including basic agents, agents with memory and knowledge bases, multi-agent systems, web interfaces, and interactive playgrounds.

## Description

This project serves as a playground for exploring the capabilities of the Agno framework, which is designed for building intelligent AI agents. The repository contains multiple examples demonstrating different aspects of agent development:

- **Basic Agents**: Simple agent implementations with tool integrations
- **Memory-Enabled Agents**: Agents with persistent knowledge bases using vector databases
- **Multi-Agent Systems**: Collaborative agent teams for complex tasks
- **Web Interfaces**: Streamlit-based user interfaces for agent interactions
- **Playground Applications**: Interactive web applications for testing multiple agents

All examples utilize OpenAI's GPT models and integrate various tools for enhanced functionality.

## Features

- 🤖 **Basic Agent**: Simple agent with web search capabilities
- 🧠 **Memory Agent**: Agent with PDF knowledge base and vector storage
- 👥 **Multi-Agent System**: Team of specialized agents (Web and Finance)
- 🌐 **Streamlit Interface**: Web UI for Thai cuisine expert agent
- 🎮 **Playground App**: Interactive FastAPI-based playground for multiple agents
- 🔍 **Tool Integrations**: DuckDuckGo search, Yahoo Finance, PDF processing
- 💾 **Persistent Storage**: SQLite and LanceDB for agent memory
- 📊 **Data Visualization**: Table-based financial data display

## Project Structure

```
Agno_tryout/
├── agent.py                 # Basic agent with DuckDuckGo tools
├── Agent_Memory.py          # Agent with Thai recipes knowledge base
├── agent_memory_st.py       # Streamlit web app for Thai cuisine expert
├── multiagents.py           # Multi-agent system for market analysis
├── playground.py            # FastAPI playground app with multiple agents
├── requirements.txt         # Python dependencies
├── .gitignore              # Git ignore rules
├── LICENSE                 # MIT License
└── README.md               # This file
```

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Monish-Nallagondalla/Agno_tryout.git
   cd Agno_tryout
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables:**
   Create a `.env` file in the root directory and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

## Usage

### Basic Agent (`agent.py`)
Run a simple agent that can search the web and answer questions:

```bash
python agent.py
```

This agent uses DuckDuckGo for web searches and can answer general questions.

### Memory Agent (`Agent_Memory.py`)
Run an agent with a knowledge base of Thai recipes:

```bash
python Agent_Memory.py
```

This agent:
- Loads Thai recipes from a PDF knowledge base
- Uses LanceDB for vector storage
- Can answer questions about Thai cuisine and recipes
- Falls back to web search for additional information

### Streamlit Web App (`agent_memory_st.py`)
Launch the web interface for the Thai cuisine expert:

```bash
streamlit run agent_memory_st.py
```

Open your browser to `http://localhost:8501` to interact with the agent through a user-friendly interface.

### Multi-Agent System (`multiagents.py`)
Run a team of agents for comprehensive market analysis:

```bash
python multiagents.py
```

This system includes:
- **Web Agent**: Searches for general information
- **Finance Agent**: Retrieves stock data and financial metrics
- Analyzes market outlook and provides investment recommendations

### Playground App (`playground.py`)
Launch the interactive playground with multiple agents:

```bash
python playground.py
```

This starts a FastAPI server at `http://localhost:8000` with:
- Web interface for interacting with agents
- Persistent storage for conversation history
- Support for both web search and financial data agents

## Examples

### Basic Agent Query
```python
agent.print_response("What is the latest score of India vs New Zealand CT 2025 final", stream=True)
```

### Memory Agent with Knowledge Base
```python
agent.print_response("How do I make chicken and galangal in coconut milk soup", stream=True)
agent.print_response("What is the history of Thai curry?", stream=True)
```

### Multi-Agent Market Analysis
```python
agent_team.print_response("analyze the market outlook and financial performance of AI semiconductor company NVDA And Tesla And suggest whether I have to buy or not?", stream=True)
```

## Dependencies

Key dependencies include:

- **agno**: Core framework for building AI agents
- **openai**: OpenAI API integration
- **streamlit**: Web interface framework
- **duckduckgo-search**: Web search functionality
- **yfinance**: Yahoo Finance data retrieval
- **lancedb**: Vector database for knowledge storage
- **pypdf**: PDF processing for knowledge bases
- **fastapi**: Web framework for playground app
- **sqlalchemy**: Database ORM for agent storage

See `requirements.txt` for complete list of dependencies.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## Author

**Monish Nallagondalla**

- GitHub: [@Monish-Nallagondalla](https://github.com/Monish-Nallagondalla)
- LinkedIn: [Your LinkedIn Profile] (if applicable)

---

*Built with ❤️ using the Agno framework*
