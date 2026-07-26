# 🤖 Supervisor Multi-Agent AI Assistant

A hierarchical multi-agent AI assistant built using **Strands Agents**, **Ollama**, and **Streamlit**. The system uses a **Supervisor Agent** to intelligently route user requests to specialized agents, each equipped with its own tools to solve domain-specific tasks.

---

## 📌 Features

- 🧠 Supervisor-based multi-agent orchestration
- 🔍 Research Agent with Search and PDF tools
- 💻 Coding Agent with Python execution and File tools
- 🧮 Math Agent with Calculator tool
- 🤖 Local LLM inference using Ollama (Llama 3.2)
- 🎨 Interactive Streamlit frontend
- 📄 PDF document reading and summarization
- 🔄 Modular and scalable architecture

---

## 🏗️ Architecture

```text
                           User
                             │
                             ▼
                    Supervisor Agent
                             │
        ┌────────────────────┼────────────────────┐
        ▼                    ▼                    ▼
   Research Agent      Coding Agent         Math Agent
        │                    │                    │
   ┌────┴────┐          ┌────┴────┐         ┌────┴────┐
   ▼         ▼          ▼         ▼         ▼
 Search     PDF     Python Tool  File Tool Calculator
```

## 🚀 Tech Stack

- Python 3.11+
- Strands Agents
- Ollama
- Llama 3.2
- Streamlit
- DuckDuckGo Search
- PyPDF

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/Supervisor-Multi-Agent-AI-Assistant.git

cd Supervisor-Multi-Agent-AI-Assistant
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Install and Run Ollama

Download Ollama:

https://ollama.com/download

Pull the Llama 3.2 model:

```bash
ollama pull llama3.2
```

Start Ollama:

```bash
ollama serve
```

---

### 5. Configure the Model

Update `config.py`

```python
from strands.models.ollama import OllamaModel

model = OllamaModel(
    host="http://localhost:11434",
    model_id="llama3.2"
)
```

---

## ▶️ Running the Project

### Run the Streamlit Frontend

```bash
streamlit run frontend.py
```

---

## 💬 Example Queries

### Research

```
Explain Amazon Bedrock.
```

```
Explain LangGraph architecture.
```

```
Summarize the uploaded PDF.
```

---

### Coding

```
Write Python code for Binary Search.
```

```
Debug this Python function.
```

```
Explain the code.
```

---

### Math

```
Calculate (4567 * 345) / 78
```

```
Solve x² + 5x + 6 = 0
```

---

## 🔄 Workflow

```text
User Query
      │
      ▼
Supervisor Agent
      │
      ▼
Specialized Agent
      │
      ▼
Appropriate Tool
      │
      ▼
Tool Output
      │
      ▼
Specialized Agent
      │
      ▼
Final Response
```

---

## 🎯 Agents

### 🧠 Supervisor Agent

Responsibilities:

- Understand the user's request
- Route requests to the appropriate specialist
- Coordinate multiple agents when required
- Return the final response

---

### 🔍 Research Agent

Responsibilities:

- Technical explanations
- AI and Cloud concepts
- Architecture explanations
- PDF summarization

Tools:

- Search Tool
- PDF Tool

---

### 💻 Coding Agent

Responsibilities:

- Python programming
- Code generation
- Debugging
- File operations

Tools:

- Python Tool
- File Tool

---

### 🧮 Math Agent

Responsibilities:

- Mathematical calculations
- Equation solving
- Arithmetic operations

Tools:

- Calculator Tool

---

## 🔧 Future Enhancements

- Amazon Bedrock AgentCore integration
- Memory support
- Multi-step planning
- Streaming responses
- Conversation history persistence
- Authentication
- Docker deployment
- Additional specialized agents

---

## 📸 Demo

Future screenshots of the Streamlit interface can be added here.

---

## 📚 Learning Outcomes

This project demonstrates:

- Multi-Agent Systems
- Supervisor Pattern
- Hierarchical Agent Architecture
- Tool Calling
- Agent Orchestration
- Local LLM Integration
- Streamlit UI Development
- Modular AI Application Design

---

## 👨‍💻 Author

**Sahana**

AI/ML Engineer

---

## ⭐ Acknowledgements

- Strands Agents
- Ollama
- Streamlit
- DuckDuckGo Search
