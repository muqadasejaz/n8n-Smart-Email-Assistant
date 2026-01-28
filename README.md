# Smart Email Assistant 

<img width="1584" height="396" alt="n8n" src="https://github.com/user-attachments/assets/1e531527-a9b0-433d-8143-1dcd3a0aa558" />


## Project Overview

Smart Email Assistant is an automated Gmail workflow built with n8n that classifies incoming emails by priority, applies appropriate labels, and takes intelligent actions such as drafting replies, sending auto-responses, or suggesting passive handling for low-importance emails.

It is designed for professionals who want to reduce inbox overload while ensuring that critical job and work-related emails are handled promptly and correctly.

---

## What This Automation Does

- Monitors incoming Gmail messages in real time  
- Extracts structured email data (sender, subject, body, metadata)  
- Classifies emails into High, Medium, or Low priority using keyword-based logic  
- Applies Gmail labels automatically  
- Uses an LLM to draft professional replies for important emails  
- Sends auto-replies for high-priority messages  
- Creates drafts for medium-priority learning or career emails  
- Suggests actions for low-priority promotional emails  

---

## Key Features

- **Priority Classification Engine**
  - High Priority: Job offers, interviews, deadlines, clients, contracts
  - Medium Priority: Courses, learning resources, certifications
  - Low Priority: Promotions, sales, advertisements

- **Automated Gmail Labeling**
  - High Priority: IMPORTANT + STARRED
  - Medium Priority: IMPORTANT
  - Low Priority: No labels applied

- **AI-Powered Email Drafting**
  - Professional replies for work-related emails
  - Polite follow-ups for learning opportunities
  - Action suggestions for promotions

- **Smart Reply Handling**
  - Auto-send replies for high-priority emails
  - Save drafts for medium-priority emails
  - Recommend archive or ignore for low-priority emails

- **Fail-Safe Parsing**
  - Robust JSON parsing with graceful fallbacks
  - Prevents workflow crashes on malformed AI responses

---

## Tools Used

- **n8n** – Workflow orchestration and automation
- **Gmail API** – Email triggering, labeling, drafting, and sending
- **OpenAI (GPT-4o-mini)** – Natural language understanding and response generation
- **JavaScript (Code Nodes)** – Email parsing, classification logic, and data transformation

---

## Workflow Architecture

1. **Gmail Trigger**
   - Polls inbox every minute for new emails

2. **Email Extraction**
   - Parses sender, recipient, subject, body, and metadata

3. **Priority Classification**
   - Keyword-based scoring assigns category:
     - `0` → High Priority
     - `1` → Medium Priority
     - `2` → Low Priority

4. **Routing by Priority**
   - Switch node routes emails based on category

5. **Label Application**
   - Applies Gmail labels according to priority level

6. **AI Processing**
   - High Priority: Drafts a professional reply
   - Medium Priority: Drafts a learning-focused response
   - Low Priority: Generates an action suggestion

7. **Response Parsing**
   - Converts AI output into structured JSON

8. **Final Actions**
   - High Priority: Auto-send reply
   - Medium Priority: Create Gmail draft
   - Low Priority: Suggest archive or ignore

---

## Workflow Output

### Full Workflow Overview

<img width="1876" height="835" alt="Full Workflow" src="https://github.com/user-attachments/assets/237d1939-6e77-4bac-b4b3-9649f1038c33" />


### High Priority Emails
- Gmail labels applied
- AI-generated professional reply
- Reply automatically sent to sender

- **Output**
  
 <img width="1607" height="571" alt="high Pri" src="https://github.com/user-attachments/assets/5d64ceea-1f72-4d6a-bdb6-2b7839f9fd70" />


### Medium Priority Emails
- Gmail label applied
- AI-generated response saved as a draft
- Manual review before sending

-  **Output**

<img width="1613" height="904" alt="Medium" src="https://github.com/user-attachments/assets/b1c713b2-101b-4605-8686-6fffd0ebe809" />


### Low Priority Emails
- No reply sent
- Suggested action (Archive, Save for Later, Ignore)

---

## Workflow JSON File

You can import this workflow directly into n8n.

**Workflow File:**  

`Smart Email Assistant.json`

### Import Steps

1. Open n8n  
2. Go to **Settings → Import workflow**  
3. Upload the JSON file  

----

## Use Cases

- Job seekers managing recruiter emails
- Professionals handling high-volume inboxes
- Engineers and learners tracking courses and certifications
- Anyone who wants an AI-assisted inbox without losing control

----

## 👤 Author

Muqadas Ejaz

BS Computer Science (AI Specialization)

AI/ML Engineer

Data Science & Gen AI Enthusiast

📫 Connect with me on [LinkedIn](https://www.linkedin.com/in/muqadasejaz/)  

🌐 GitHub: [github.com/muqadasejaz](https://github.com/muqadasejaz)

📬 Kaggle: [Kaggle Profile](https://www.kaggle.com/muqaddasejaz) 

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📎 License

This project is open-source and available under the [MIT License](LICENSE).

 If you find this project useful, don’t forget to star ⭐ the repository!
