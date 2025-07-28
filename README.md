# 📚 Study Buddy – Your Personalized AI Academic Assistant (Langflow Project)

Study Buddy is an AI-powered assistant built using Langflow. It helps students manage their academic life with features like summarizing notes, generating study plans, answering subject-related questions, and finding high-quality references -- all through simple, natural prompts.

---

## 🔧 How It Works

This Langflow project uses **Groq** as the model provider and the `moonshotai/kimi-k2-instruct` model. It uses 4 intelligent agents, each connected to a unique prompt template and a decision routing system:

### 🧩 Components Used:
- **Chat Input**
- **If-Else Router** (routes commands like `/summarize`, `/plan`, `/subject`, `/resource` )
- **Prompt Templates** (for each agent)
- **Groq Language Model**
- **Agent Node**
- **Chat Output**

---

## 🤖 Main Agents

### 📄 Summarizer Agent  
**Command:** `/summarize`  
**Prompt:**  
> Please summarize the following text for a student. Use bullet points and keep the summary concise.  
> Text: `{input}`

---

### 🗓️ Planner Agent  
**Command:** `/plan`  
**Prompt:**  
> You are a helpful and organized planning assistant for a student. Based on the user’s {input}, do one of the following:
> 
> 1. If the user wants to create a planner, ask for their subjects, deadlines, and preferred pace. Then generate a simple daily or weekly plan.  
> 2. If the user asks to add a task, include it in their to-do list or calendar.  
> 3. If the user wants to remove a task, confirm and remove it from the list.  
> 4. If they ask to view or update their schedule, return the updated planner or to-do list.  
> 
> Always respond in a friendly, motivating tone. Use bullet points or checklists when listing tasks.

---

### 📘 Subject Expert + Quiz Generator Agent  
**Command:** `/subject`  
**Prompt:**  
> You are a helpful academic tutor. Based on the following topic or lesson, create a short quiz to help students review. Provide multiple-choice options and highlight the correct answer after each question.  
>  
> Topic: `{input}`

---

### 🔍 Resource Agent  
**Command:** `/resource`  
**Prompt:**  
> Find three trustworthy academic resources related to: `{input}`. Prioritize peer-reviewed or educational sources. List titles and direct links.

---

## 🧠 Expand Study Buddy

If you would like, you can also add more agents to make your own Study Buddy even more personalized and powerful. I can't stress enough how easy it is to make one — with just a few drag-and-drop components and thoughtful prompts, you can create your own AI-powered academic assistant in minutes.

### 🌟 Example Agent Ideas:
- 📆 **Exam Countdown Agent**: Tracks days left until your next exam.
- 🧘 **Wellness Check-In Agent**: Offers reminders for breaks and mental health tips.
- 📈 **Progress Tracker Agent**: Analyzes past study patterns and suggests improvements.
- 💬 **Language Translator Agent**: Translates summaries or tasks into another language.

---

## 🗝️ Setup Instructions

1. Export your flow from Langflow as `.json`.
2. In Langflow:
   - Select **Groq** as the model provider.
   - Use model: `moonshotai/kimi-k2-instruct`
   - Insert your **Groq API Key** (You can get it by searching “Groq API Key” online).
3. Import the flow and run it inside your Langflow environment.

---

## 👋 Created By

Matt James Fortes  
Electrical Engineering Student | University of Doha for Science and Technology  
2025

---
