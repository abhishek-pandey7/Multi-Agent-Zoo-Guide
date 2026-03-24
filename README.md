#  Zoo Tour AI Agent

A multi-agent AI system that acts as an intelligent zoo guide, built using Google ADK and deployed on Cloud Run.
The system leverages tool-based reasoning and sequential agent workflows to deliver rich, contextual responses about animals.

---

##  Overview

This project demonstrates how multiple AI agents can collaborate to solve a task:

* A **Greeter Agent** captures user input and manages state
* A **Research Agent** gathers information using external tools (Wikipedia)
* A **Formatter Agent** converts raw data into a structured, user-friendly response

The system is deployed as a scalable backend service using Google Cloud Run.

---

##  Architecture

```
User Input
   ↓
Greeter Agent
   ↓ (stores prompt in state)
Research Agent
   ↓ (uses tools like Wikipedia)
Formatter Agent
   ↓
Final Response
```

---

##  Features

*  Multi-agent architecture (sequential workflow)
*  Tool integration using LangChain (Wikipedia API)
*  Stateful interaction handling
*  Serverless deployment using Cloud Run
*  LLM-powered responses using Gemini (Vertex AI)

---

##  Tech Stack

* Python
* Google ADK
* Cloud Run
* Vertex AI (Gemini)
* LangChain

---

##  Demo

<img width="1374" height="571" alt="image" src="https://github.com/user-attachments/assets/8ba821f5-5986-4284-b0cc-7a6b5e970096" />
<img width="1285" height="705" alt="image" src="https://github.com/user-attachments/assets/95a3f480-7ac8-4203-b843-969af61cf211" />


* Example user query and response
* Agent workflow / tool usage

---

##  Setup

### 1. Clone the repository

```
git clone https://github.com/YOUR_USERNAME/zoo-tour-ai-agent.git
cd zoo-tour-ai-agent
```

### 2. Install dependencies

```
pip install -r requirements.txt
```

### 3. Create `.env` file

```
PROJECT_ID=your-project-id
MODEL=gemini-2.5-flash
```

---

##  Deployment

This project was deployed using Google ADK:

```
uvx --from google-adk==1.14.0 \
adk deploy cloud_run \
  --project=YOUR_PROJECT_ID \
  --region=YOUR_REGION \
  --service_name=zoo-tour-guide
```

---

##  Example Queries

* “Tell me about lions”
* “What do polar bears eat and where can I find them in the zoo?”
* “Compare elephants and giraffes”

---

##  Learnings

* Designing multi-agent workflows
* Tool-based reasoning with LLMs
* Managing shared state across agents
* Deploying AI systems on serverless infrastructure

---

##  Note

Cloud resources used for this project were cleaned up after deployment to avoid unnecessary billing.

---

##  Future Improvements

* Add internal zoo database integration
* Improve error handling for tool responses
* Add memory for multi-turn conversations
* Build a frontend UI
* Support more external knowledge sources

---

##  Author

Abhishek Pandey
