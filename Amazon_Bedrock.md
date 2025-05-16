# Amazon Bedrock

- Amazon Bedrock is a fully managed, serverless service from AWS
- Makes base Foundation Models from Amazon and third-party model providers accessible through an API

<img width="1186" alt="image" src="https://github.com/user-attachments/assets/5d7883ef-8f35-42cc-9e35-879d69894962" />

#### How does Amazon Bedrock work – High Level ?

<img width="780" alt="image" src="https://github.com/user-attachments/assets/ed101312-38c4-463b-a214-e0a7e3e72765" />

#### Key features of Foundation Models Amazon Bedrock supports

<img width="750" alt="image" src="https://github.com/user-attachments/assets/853e07a0-2a33-42ff-8b65-94ce84806cf5" />

#### Bedrock Builder Tools

| **Builder Tool**           | **Description**                                                                 | **Use When**                                                                 | **Example Use Case**                                                                 |
|----------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **Agents**                 | Define task-oriented agents that can call APIs, manage memory, and reason through goals. | You need autonomous task execution via APIs or functions.                   | Build a virtual assistant that checks order status using an API call.                |
| **Knowledge Bases**        | Connect models to your private data using RAG (Retrieval-Augmented Generation). | You want accurate responses grounded in internal documents or FAQs.         | Enable a customer support bot to answer using product manuals and help docs.         |
| **Prompt Management**      | Create, version, test, and manage prompts centrally across teams.                | You want consistent, reusable prompts for apps or workflows.                | Manage and A/B test prompts for multiple LLM-based customer-facing applications.     |
| **Model Evaluation**       | Evaluate models for accuracy, bias, toxicity, and performance using test sets.  | You need to benchmark model behavior before deployment.                     | Compare Titan vs. Claude models on tone and factual accuracy for internal use.       |
| **Guardrails**             | Define content filtering, tone, and sensitive topic controls to enforce safety. | You want to ensure responsible AI usage and policy compliance.              | Restrict a healthcare chatbot from discussing medical diagnoses or sensitive topics. |
| **Bedrock Flows** *(preview)* | Visual tool to build multi-step workflows with branching logic and LLM actions.   | You need to orchestrate LLM + tools in a no-code/low-code environment.      | Create a loan pre-approval workflow using model calls + document processing steps.   |

