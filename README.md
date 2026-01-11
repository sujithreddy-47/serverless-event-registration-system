🌐 Serverless Event Registration System
with AI-Powered Connection Matching

A 100% serverless, cloud-native event management platform built on Amazon Web Services (AWS) that goes beyond traditional event registration by integrating AI-driven networking, recommendations, and chatbot support.

📌 Project Overview

Traditional event platforms suffer from:

High server costs

Poor scalability during traffic spikes

Lack of meaningful attendee networking

This project solves these issues by implementing a fully serverless AWS architecture combined with custom AI algorithms to enhance user engagement and networking value.

🚀 Key Features
🔹 Serverless Architecture

No EC2 servers

Auto-scaling, pay-as-you-go model

Zero idle cost

🔹 AI-Powered Features

DNA Matching System – connects attendees based on skills, interests, goals, and mentorship needs

Hybrid Event Recommendation Engine – personalized event suggestions

NLP-based AI Chatbot – instant, context-aware responses

🔹 Admin Dashboard

Real-time event analytics

User engagement metrics

Registration trends

🏗️ System Architecture

Frontend

React.js

Hosted on Amazon S3

Globally delivered via Amazon CloudFront

Backend

Amazon API Gateway (REST APIs)

AWS Lambda (Python 3.12)

Database

Amazon DynamoDB

Events

Registrations

MatchingProfiles (with GSI on eventId)

Monitoring

Amazon CloudWatch

🧠 AI Modules Explained
🧬 DNA Matching System

Calculates compatibility using:

Shared interests (30%)

Mentorship alignment (25%)

Goal similarity (25%)

Collaboration intent (15%)

Same-organization penalty (−10%)

Also generates personalized ice-breaker messages to help users start conversations naturally.

🤖 AI Event Recommendation Engine

A 4-factor hybrid model:

40% Collaborative filtering

30% Category similarity

20% Popularity

10% Urgency (event filling fast)

Returns top 3 personalized event suggestions.

💬 AI Chatbot

Keyword-based intent detection

Fuzzy matching for event names

Context-aware responses based on event type (hackathon, workshop, etc.)

🔐 Security Design

IAM Roles with least-privilege access

HTTPS (SSL/TLS) via CloudFront

S3 protected using Origin Access Identity (OAI)

Amazon Cognito planned for authentication

CORS handled at API Gateway + Lambda level

📊 Performance & Cost
⚡ Performance

API response time < 500 ms

DynamoDB single-digit millisecond latency

Global low-latency delivery via CloudFront

💰 Cost Efficiency

Runs mostly within AWS Free Tier

Example: 1,000 registrations ≈ <$0.20

Zero cost during idle periods

🛠️ Technologies Used

AWS Lambda

Amazon API Gateway

Amazon DynamoDB

Amazon S3

Amazon CloudFront

Amazon SES

Amazon IAM

Amazon CloudWatch

React.js

Python

👨‍💻 Contributors

Byna Sriroop (23BCE1863)

Frontend Development

DNA Matching System

Admin Dashboard

Deployment (S3 + CloudFront)

Gunnam Reddy Sujith Reddy (23BCE1613)

Backend Architecture

API Gateway & IAM

AI Event Recommendation Engine

AI Chatbot

End-to-End Registration Workflow

🔮 Future Enhancements

Integrate Amazon Lex for advanced NLP

Enable automated email reminders using SES + CloudWatch Events

Add full Admin CRUD operations

Implement CI/CD pipeline (AWS CodePipeline / Terraform)

📚 References

AWS Official Documentation:

AWS Lambda

DynamoDB

API Gateway

CloudFront

S3

Cognito

SES
