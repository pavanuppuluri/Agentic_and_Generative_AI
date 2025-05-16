# Creating A Custom Model

#### Usecase

You want to build a text summarization app which captures the conversation between Physician & Patient,
converts that voice into text and summarises it.

**What if we use base model for this?**

Problem is, as base model is trained on generic internet data, may be it won't understand the Domain terminology.
In this case, we can create a Custom Model using below options

<img width="840" alt="image" src="https://github.com/user-attachments/assets/62755ab2-f74d-4a65-9d26-5de73106d6da" />

<img width="851" alt="image" src="https://github.com/user-attachments/assets/279432a0-db5f-4e27-9080-e4cf0a5897d9" />

| **Customization Method**     | **Description**                                                                 | **Use When**                                                             | **Example Use Case**                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **Fine-Tuning**              | Train the foundation model on labeled, task-specific data to tailor its behavior. | You need precise output aligned with specific tasks or brand tone.        | Fine-tune Titan on customer support chat logs to create a brand-aligned chatbot.    |
| **Knowledge Distillation**   | Compress a large (teacher) model into a smaller (student) model to reduce cost and latency. | You want cheaper, faster inference. You’ve fine-tuned a large model and want to deploy it in resource-constrained environments       | Deploy a smaller, faster version of a fine-tuned model for mobile customer support. |
| **Continued Pre-training**   | Further pretrain a foundation model on large amounts of unlabeled, domain-specific data. | You have lots of domain data but no labels, and want better vocabulary alignment. | Pretrain Titan with thousands of financial reports to enhance financial understanding. |


