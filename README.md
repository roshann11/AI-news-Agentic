
# End-to-End Agentic AI Chatbots with LangGraph and Streamlit

This repository provides a boilerplate for building and deploying agentic AI chatbots using a modern stack of technologies, including LangGraph, Streamlit, and Groq LLM. The project is designed to be modular, scalable, and easy to customize for various use cases.

## 🌟 Key Features

- **Modular and Scalable Architecture**: The project is organized into distinct modules for UI, language models, graph construction, and tools, making it easy to extend and maintain.
- **Multiple LLM Integrations**: Easily switch between different language models. The current implementation includes Groq LLM for fast and efficient responses.
- **Stateful, Multi-Agent Applications**: Built with LangGraph, this project allows for the creation of complex, stateful, and multi-agent applications that can handle a wide range of tasks.
- **Customizable Chatbot Modes**: The application supports multiple chatbot modes, including:
  - **AI News**: Fetches and summarizes the latest AI news.
  - **Basic Chatbot**: A simple conversational agent.
  - **Chatbot with Tools**: An agent that can use tools (e.g., web search) to answer questions.
- **User-Friendly Web Interface**: A clean and intuitive user interface built with Streamlit, allowing for easy interaction with the chatbots.

## 📂 Project Structure

The project is organized into the following directories and files:

```
AINEWSAgentic/
├── app.py                  # Main application entry point
├── README.md               # This file
├── requirements.txt        # Python dependencies
├── AINews/                 # Directory for storing AI news summaries
│   ├── daily_summary.md
│   ├── monthly_summary.md
│   └── weekly_summary.md
└── src/
    ├── __init__.py
    └── langgraphagenticai/
        ├── __init__.py
        ├── main.py             # Main logic for the agentic AI application
        ├── graph/
        │   ├── __init__.py
        │   └── graph_builder.py # Constructs the agentic graph
        ├── LLMS/
        │   ├── __init__.py
        │   └── groqllm.py      # Groq LLM integration
        ├── nodes/
        │   ├── __init__.py
        │   ├── ai_news_node.py # Node for fetching AI news
        │   ├── basic_chatbot_node.py # Node for the basic chatbot
        │   └── chatbot_with_Tool_node.py # Node for the tool-using chatbot
        ├── state/
        │   ├── __init__.py
        │   └── state.py        # Defines the state of the agentic graph
        ├── tools/
        │   ├── __init__.py
        │   └── search_tool.py  # Web search tool
        └── ui/
            ├── __init__.py
            ├── uiconfigfile.ini # Configuration for the UI
            ├── uiconfigfile.py  # UI configuration loader
            └── streamlitui/
                ├── display_result.py # Displays the results in the UI
                └── loadui.py         # Loads the Streamlit UI components
```

## 🚀 Getting Started

Follow these steps to set up and run the project on your local machine.

### Prerequisites

- Python 3.8 or higher
- An API key from [Groq](https://console.groq.com/)
- An API key from [Tavily](https://tavily.com/)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/AINEWSAgentic.git
   cd AINEWSAgentic
   ```

2. **Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up your environment variables:**

   Create a `.env` file in the root directory of the project and add your API keys:

   ```
   GROQ_API_KEY="your-groq-api-key"
   TAVILY_API_KEY="your-tavily-api-key"
   ```

### Running the Application

To start the application, run the following command in your terminal:

```bash
streamlit run app.py
```

This will open the application in your web browser, where you can start interacting with the chatbots.

## 📖 How to Use

The application provides a user-friendly interface with the following options:

- **Select Use Case**: Choose from the available chatbot modes:
  - **AI News**: Get the latest AI news summarized for you.
  - **Basic Chatbot**: Engage in a simple conversation.
  - **Chatbot with Tools**: Ask questions that require web search capabilities.
- **Chat Interface**: Enter your messages and receive responses from the selected chatbot.
- **Summaries**: For the AI News mode, you can view daily, weekly, and monthly summaries.

## 🏗️ Architecture Overview

The application is built around a few key components:

- **Streamlit UI**: The user interface is built with Streamlit, providing a simple and interactive way to use the application.
- **LangGraph**: The core of the application is the agentic graph, which is built using LangGraph. This graph defines the flow of control and state management for the chatbots.
- **Nodes**: Each node in the graph represents a specific function, such as fetching news, running a chatbot, or using a tool.
- **Tools**: The application can be extended with various tools, such as web search, to enhance the capabilities of the chatbots.
- **LLMs**: The language models provide the intelligence for the chatbots. The project is designed to be model-agnostic, with Groq LLM as the default.

## 📝 To-Do

- [ ] Add more LLM integrations (e.g., OpenAI, Anthropic).
- [ ] Improve the UI with more interactive features.
- [ ] Add more tools to the chatbot.
- [ ] Implement a database to store conversation history.
- [ ] Write more unit and integration tests.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue to discuss your ideas.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
