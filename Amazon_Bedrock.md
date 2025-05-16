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


## AWS Bedrock Batch Inference

### 🧪 What is Bedrock Batch Inference?

**AWS Bedrock Batch Inference** allows you to run **large-scale asynchronous inference jobs** on a batch of inputs stored in Amazon S3. Instead of processing one input at a time in real-time, batch inference efficiently processes many inputs at once, making it ideal for high-throughput and cost-effective workloads.

#### ⚙️ How It Works

1. Prepare your input data (e.g., JSONL or CSV file with prompts) and upload it to Amazon S3.  
2. Create a batch inference job in AWS Bedrock:  
   - Select the foundation model (e.g., Claude, Titan, Jurassic)  
   - Specify input and output S3 locations  
3. AWS Bedrock asynchronously processes each input record and saves the results back to your S3 output bucket.


#### ✅ Use Cases for Bedrock Batch Inference

| **Category**             | **Use Case**                                                                 |
|--------------------------|------------------------------------------------------------------------------|
| **Customer Support**     | Summarize thousands of past support tickets for insights or quality checks.  |
| **Marketing**            | Generate personalized email templates or product descriptions at scale.     |
| **HR / Resume Parsing**  | Analyze and extract skills from 10,000+ resumes to auto-rank candidates.     |
| **Legal / Compliance**   | Extract and classify clauses from large sets of contracts.                   |
| **Academic Research**    | Summarize or translate hundreds of research papers for further analysis.     |
| **Product**              | Auto-generate user-friendly product descriptions for large catalogs.         |
| **Healthcare**           | Normalize and summarize thousands of doctor’s notes or medical reports.     |
| **IT / DevOps**          | Generate documentation for 1,000+ APIs from OpenAPI specs automatically.     |


#### 🚀 Benefits

- Cost-efficient for large jobs compared to real-time inference.  
- Scales to millions of input records.  
- Asynchronous processing lets you retrieve results once the job completes without waiting.  


# Amazon Bedrock - Architecture

<img width="1062" alt="image" src="https://github.com/user-attachments/assets/318afb5f-2a89-4979-8f27-e451079b731a" />

**Runtime Inference** : Used to redirect to right model endpoint based on the API request

**Example.**
```json
body = json.dumps({
    "prompt": user_prompt,
    "temperature": 0.9,
    "max_tokens": 400
}),
contentType = "application/json",
accept = "*/*",
modelId = 'cohere.command-text-v14'

```

















