# AI-Powered-Interview-Question-Generator-Evaluator-System

**Project Overview**
This project implements an AI-powered, multi-agent interview system using LangChain and Azure OpenAI. The system automates key stages of the technical interview process, including job description analysis, interview question generation, candidate answer evaluation, and final hiring recommendations.

Each stage of the interview process is handled by a specialized LangChain agent, coordinated through a central orchestration layer. Session memory is used to preserve interview context, and a rule-guided decision layer ensures consistent and explainable hiring outcomes.

**System Architecture**

The system follows a multi-agent workflow, where each agent has a clearly defined responsibility:

**Job Description Analyzer Agent** Extracts required skills, responsibilities, and role expectations from the job description.

**Interview Question Generator Agent** Generates structured, role-specific interview questions based on extracted role insights.

**Candidate Answer Evaluation Agent** Objectively evaluates candidate responses and assigns structured scores across technical, system design, cloud, and behavioral dimensions.

**Hiring Recommendation Agent** Produces a final Hire / No-hire / Irrelevant decision using rule-guided logic based on evaluation scores.

A centralized orchestration function coordinates these agents in a defined sequence


**Agent Orchestration & Memory**

The workflow is orchestrated through a single controller function that executes agents sequentially:
1.Job description analysis
2.Question generation
3.Candidate answer evaluation
4.Final hiring recommendation
Session memory (ConversationBufferMemory) is used to retain context across interview stages, ensuring consistency throughout the interview session.


**Output**

The system generates:
1.Role-specific interview questions
2.Structured JSON-based candidate evaluations
3.Final hiring recommendations
**4.Tabular comparison of multiple candidates**
