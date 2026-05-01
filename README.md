# System Design Case Study

---

# 🧠 Q1. AI Resume Screening System

## 📌 Scenario
Startups build an AI recruitment platform for:
- Resume screening  
- Candidate ranking  
- Interview scheduling  
- High daily volume  

---

## ⚠️ Constraints

- Heavy compute (AI models)  
- Sensitive data (privacy concerns)  
- Limited budget  
- Needs careful system design  

---

## 🎯 Tasks

- Choose cloud deployment and service model  
- Design AI processing approach  
- Define storage & processing pipeline  

---

## 🔍 Focus Areas

- Serverless vs Containers  
- Batch vs Real-time processing  

---

# ✅ Solution

## ☁️ 1. Cloud Deployment & Service Model

### 🔹 Deployment Model: Hybrid Cloud

- **Public Cloud**
  - AI training & inference  
  - Scalable and cost-efficient  

- **Private Cloud / VPC**
  - Store sensitive data (PII, resumes)  

### 👉 Why?

- Protects sensitive data  
- Enables scalable compute  

---

### 🔹 Service Model

- **SaaS**
  - Recruiter dashboard  
- **PaaS**
  - AI model deployment & APIs  
- **IaaS (limited)**
  - GPU workloads  

### 👉 Final Choice

**SaaS + PaaS + selective IaaS**

---

## 🤖 2. AI Processing Approach

### 🔹 Microservices Architecture

- Resume Parser (NLP)  
- Ranking Model  
- Interview Scheduler  
- Notification Service  

---

### 🔹 Processing Strategy: Hybrid

#### ✔ Batch
- Bulk uploads  
- Model training  

#### ✔ Real-Time
- Instant resume scoring  
- Live ranking  

### 👉 Why?

- Batch = cost-efficient  
- Real-time = better UX  

---

### 🔹 Model Strategy

- Pre-trained NLP models (fine-tuned)  
- Keyword extraction  
- Semantic matching  
- Scoring system  

---

## 🗄️ 3. Storage & Pipeline

### 🔹 Storage

- Object Storage → resumes  
- Database → structured data  
- Redis Cache → fast ranking access  

---

### 🔹 Pipeline Flow

1. Upload → API Gateway  
2. Store in object storage  
3. Trigger processing  
4. NLP parsing  
5. AI scoring  
6. Store results  
7. Display dashboard  

---

## ⚙️ 4. Serverless vs Containers

| Use Case | Best Option |
|----------|------------|
| Event-driven tasks | Serverless |
| AI models (heavy compute) | Containers |

### 👉 Why?

- Serverless → cost-efficient  
- Containers → GPU + ML control  

---

## ⏱️ 5. Batch vs Real-Time

| Feature | Batch | Real-Time |
|--------|------|----------|
| Bulk uploads | ✅ | ❌ |
| Instant scoring | ❌ | ✅ |
| Model training | ✅ | ❌ |

### 👉 Final: Hybrid approach  

---

## 🚀 6. Optimization

- GPU instances for inference  
- Auto-scaling  
- Spot instances (cost saving)  
- Cache top candidates  
- Lightweight models for real-time  

---

## 🔒 7. Security

- Encryption (AES-256, TLS)  
- RBAC access control  
- Data isolation  
- GDPR compliance  
- Monitoring & logging  

---

# 🎬 Q2. OTT Streaming Platform

## 📌 Scenario

Video platform with:
- HD / 4K streaming  
- Recommendations  
- Multi-device access  
- Subscription model  

---

## ⚠️ Constraints

- High bandwidth  
- Global scalability  
- Zero buffering expectation  
- Large storage  

---

## 🎯 Tasks

- Design video delivery system  
- Select cloud model  
- Plan global scaling  

---

## 🔍 Focus Areas

- CDN & edge delivery  
- Distributed storage  
- Auto-scaling  
- Recommendation system  

---

# ✅ Solution

## ☁️ 1. Cloud Model

- **Public Cloud (Multi-region)**  

### Service Model

- **PaaS**
  - Streaming services  
  - Recommendation system  

- **IaaS**
  - Storage  
  - Video processing  

---

## 🎥 2. Video Delivery System

- CDN + Edge Servers  
- Cache videos near users  
- Reduce latency & buffering  

### Streaming

- HLS  
- DASH  

---

## 🌍 3. Global Scaling

- Multi-region deployment  
- Auto-scaling  
- Load balancing  

---

## 🗄️ 4. Storage Design

- Distributed object storage  
- Cross-region replication  
- Cold storage (old content)  

---

## ⚡ 5. Zero Buffering Strategy

- CDN caching  
- Adaptive bitrate streaming  
- Edge delivery  

---

## 🎯 6. Recommendation System

### Use AI/ML

Analyze:
- Watch history  
- User behavior  

### Output:
- Personalized recommendations  

---
