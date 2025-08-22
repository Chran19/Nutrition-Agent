# 📖 README – Nutrition-Agent

## Overview

**Nutrition-Agent** is an AI-powered assistant built using **IBM watsonx.ai Agent Lab** and **LangGraph**. It leverages large language models, retrieval-augmented generation (RAG), and external tools to provide personalized nutritional guidance. The agent is designed to answer user queries, suggest healthy food choices, track dietary habits, and reinforce positive health behavior while reminding users of essential medical disclaimers.

The project demonstrates how to:

* Authenticate with the **watsonx.ai API** using an IBM Cloud API key.
* Configure and deploy a **LangGraph-based agent** with memory, tools, and custom instructions.
* Integrate external search tools (Google, DuckDuckGo, Wikipedia, WebCrawler, Weather).
* Add a RAG (retrieval augmented generation) tool for domain-specific knowledge grounding.
* Define conversational strategies (greetings, clarification prompts, encouragement, proactive suggestions, and hydration reminders).

---

## Features

* 🧠 **Conversational Agent** – Built on watsonx.ai Granite 3.3 8B Instruct model.
* 📚 **Knowledge Tools** – Access to Google Search, DuckDuckGo, Wikipedia, WebCrawler, and RAG.
* 🌦️ **Utility Tools** – Weather integration for context-aware nutrition advice.
* 💧 **Hydration Reminders** – Periodic prompts to encourage proper water intake.
* 🍎 **Nutrient Education** – Clear explanations of macronutrients, micronutrients, and balanced diet principles.
* ⚠️ **Medical Disclaimer** – Always reminds users that it’s not a substitute for professional medical advice.
* 📝 **Memory Support** – Saves conversation history for continuity.

---

## Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Chran19/Nutrition-Agent.git
cd Nutrition-Agent
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure IBM Cloud API Key

Run the notebook and enter your **IBM Cloud API key** when prompted:

```python
credentials = get_credentials()
```

### 4. Set Environment Variables

```bash
export PROJECT_ID=your_project_id
export SPACE_ID=your_space_id
```

### 5. Run the Notebook

Open Jupyter or Watson Studio and run all cells to initialize the agent.

---

## Usage

Once initialized, the agent can be invoked for interactive nutrition coaching. Example:

```python
agent = create_agent(context)

response = agent.invoke({"messages": [HumanMessage(content="What’s a good post-workout meal?")]})
print(response["messages"][-1].content)
```

---

## Example Conversations

* **Greeting:**
  💬 User: *"Hello"*
  🤖 Agent: *"Hi, I am watsonx.ai, your personal Nutrition Buddy. How can I help you achieve your health goals today?"*

* **Hydration Reminder:**
  🤖 *"Just a friendly reminder to stay hydrated! Have you had a glass of water recently?"*

* **Proactive Suggestion:**
  🤖 *"Based on your recent food logs, you might enjoy this healthy recipe for a quinoa salad."*

---

## Project Structure

```
Nutrition-Agent/
│── notebook.ipynb        # Main Watsonx Agent Lab notebook
│── README.md             # Project documentation

```

---

## Disclaimer

⚠️ **Medical Disclaimer:**
This agent is designed for educational purposes only. It is **not a substitute for professional medical advice, diagnosis, or treatment**. Always consult with a qualified healthcare provider before making dietary changes.

---

## License

MIT License – free to use and modify with attribution.
