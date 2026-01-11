# Serverless Event Registration System  
## AI-Powered Connection Matching Platform

A fully serverless, cloud-native event registration and management system built on **Amazon Web Services (AWS)**.  
This platform enhances traditional event registration by integrating **AI-based attendee matching, personalized event recommendations, and an NLP-powered chatbot**.

---

## 📖 Project Overview

Traditional event management platforms suffer from:
- High infrastructure costs
- Poor scalability during traffic spikes
- Limited networking value for attendees

This project solves these issues using a **100% serverless AWS architecture** combined with **custom AI algorithms** to deliver scalability, cost efficiency, and intelligent user engagement.

---

## 🚀 Key Features

### 🔹 Serverless Architecture
- No EC2 servers
- Auto-scaling and pay-as-you-go model
- Zero idle cost

### 🔹 AI-Powered Features
- **DNA Matching System** – connects attendees based on skills, goals, interests, and mentorship needs
- **Hybrid Event Recommendation Engine** – personalized event suggestions
- **NLP-Based AI Chatbot** – instant, context-aware user support

### 🔹 Admin Dashboard
- Real-time analytics
- Event capacity monitoring
- Registration trends and user engagement metrics

---

## 🏗️ System Architecture

### Frontend
- React.js
- Hosted on **Amazon S3**
- Delivered globally using **Amazon CloudFront**

### Backend
- **Amazon API Gateway** (REST APIs)
- **AWS Lambda** (Python 3.12)

### Database
- **Amazon DynamoDB**
  - Events table
  - Registrations table
  - MatchingProfiles table (with GSI on `eventId`)

### Monitoring & Logging
- **Amazon CloudWatch**

---

## 🧠 AI Modules Explained

### 🧬 DNA Matching System
Calculates compatibility using:
- Shared interests (up to 30 points)
- Mentorship alignment (up to 25 points)
- Goal similarity (up to 25 points)
- Collaboration intent (up to 15 points)
- Same-organization penalty (-10 points)

Also generates **personalized ice-breaker messages** to help attendees start meaningful conversations.

---

### 🤖 AI Event Recommendation Engine
A **4-factor hybrid recommendation model**:
- 40% Collaborative Filtering
- 30% Category Matching
- 20% Popularity
- 10% Urgency (event filling rate)

Returns the **top 3 personalized event recommendations**.

---

### 💬 AI Chatbot
- Keyword-based intent detection
- Fuzzy matching for event names
- Context-aware responses based on event type (hackathon, workshop, etc.)

---

## 🔐 Security Design

- IAM roles with **least-privilege access**
- HTTPS via CloudFront (SSL/TLS)
- S3 secured using **Origin Access Identity (OAI)**
- Amazon Cognito planned for authentication
- Proper CORS handling at API Gateway and Lambda

---

## 📊 Performance & Cost Efficiency

### Performance
- API response time < **500 ms**
- DynamoDB single-digit millisecond latency
- Global low-latency delivery using CloudFront

### Cost
- Runs largely within **AWS Free Tier**
- Example: 1,000 registrations cost **< $0.20**
- No cost during idle periods

---

## 🛠️ Technologies Used

- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- Amazon S3
- Amazon CloudFront
- Amazon IAM
- Amazon SES
- Amazon Cognito
- Amazon CloudWatch
- React.js
- Python

---

## 👨‍💻 Contributors

**Gunnam Reddy Sujith Reddy (23BCE1613)**  
- Frontend development & deployment  
- API Gateway & IAM configuration  
- AI Event Recommendation Engine  
- AI Chatbot  
- End-to-end registration workflow
- DNA Matching System  
- Admin Dashboard  
---

## 🔮 Future Enhancements

- Integrate **Amazon Lex** for advanced NLP
- Enable automated email reminders using **SES + CloudWatch Events**
- Add full **Admin CRUD operations**
- Implement **CI/CD pipeline** using AWS CodePipeline or Terraform

---

## 📚 References

AWS Official Documentation:
- AWS Lambda
- Amazon DynamoDB
- Amazon S3
- Amazon CloudFront
- Amazon API Gateway
- Amazon Cognito
- Amazon SES
