# 🏕️ Camp Ground - Full Stack Camping Site Application

<div align="center">

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg?style=flat-square)](https://github.com/yourusername/camp-ground)
[![Code Quality](https://img.shields.io/badge/code%20quality-A-brightgreen.svg?style=flat-square)](https://sonarcloud.io/dashboard?id=camp-ground)
[![Security Rating](https://img.shields.io/badge/security-A-brightgreen.svg?style=flat-square)](https://github.com/yourusername/camp-ground)
[![Coverage](https://img.shields.io/badge/coverage-85%25-yellowgreen.svg?style=flat-square)](https://github.com/yourusername/camp-ground)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

</div>

## 🎯 Overview

**Camp Ground** is a modern, enterprise-grade full-stack web application that enables users to discover, add, and review camping sites. Built with a robust three-tier architecture and deployed using cloud-native DevOps practices, it demonstrates real-world deployment strategies across Development, Staging, and Production environments on Amazon EKS.

### ✨ Key Features
- 🔍 **Browse Campgrounds**: Advanced search and filtering by location, amenities, and ratings
- ⭐ **User Reviews**: Comprehensive review system with ratings and photo uploads
- 📝 **Site Management**: Admin panel for campground management
- 🔐 **Secure Authentication**: JWT-based authentication with role-based access control
- 📱 **Responsive Design**: Mobile-first design for seamless cross-device experience
- 🌐 **Real-time Updates**: Live notifications and real-time data synchronization

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │    Backend      │    │    Database     │
│   (React.js)    │◄──►│  (Node.js +     │◄──►│   (MongoDB)     │
│                 │    │   Express.js)   │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 │
                    ┌─────────────────┐
                    │   Load Balancer │
                    │   (AWS ALB)     │
                    └─────────────────┘
```

### 🎯 Three-Tier Architecture Components

#### 🎨 **Presentation Tier (Frontend)**
- **Technology**: React 18 with TypeScript
- **State Management**: Redux Toolkit + RTK Query
- **Styling**: Tailwind CSS with custom components
- **Build Tool**: Vite for optimized builds
- **Testing**: Jest + React Testing Library

#### ⚙️ **Application Tier (Backend)**
- **Framework**: Node.js with Express.js
- **Authentication**: JWT with refresh token rotation
- **API Design**: RESTful APIs with OpenAPI 3.0 documentation
- **Middleware**: Rate limiting, CORS, helmet security headers
- **File Storage**: AWS S3 for image uploads

#### 💾 **Data Tier (Database)**
- **Primary Database**: MongoDB with Mongoose ODM
- **Caching**: Redis for session management and caching
- **Search**: Elasticsearch for advanced search capabilities
- **Backup**: Automated daily backups to AWS S3

## 🛠️ Technology Stack

<div align="center">

### **Fullstack Technologies**
![React](https://img.shields.io/badge/react-v18.2.0-61DAFB?style=flat-square&logo=react)
![TypeScript](https://img.shields.io/badge/typescript-v4.9.4-3178C6?style=flat-square&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/tailwindcss-v3.2.4-06B6D4?style=flat-square&logo=tailwindcss)
![Vite](https://img.shields.io/badge/vite-v4.0.0-646CFF?style=flat-square&logo=vite)
![Node.js](https://img.shields.io/badge/node.js-v18.12.1-339933?style=flat-square&logo=node.js)
![Express](https://img.shields.io/badge/express-v4.18.2-000000?style=flat-square&logo=express)
![MongoDB](https://img.shields.io/badge/mongodb-v6.0-47A248?style=flat-square&logo=mongodb)
![Redis](https://img.shields.io/badge/redis-v7.0-DC382D?style=flat-square&logo=redis)

### **DevOps & Cloud**
![AWS](https://img.shields.io/badge/AWS-EKS%20%7C%20EC2%20%7C%20S3-FF9900?style=flat-square&logo=amazon-aws)
![Docker](https://img.shields.io/badge/docker-v20.10-2496ED?style=flat-square&logo=docker)
![Kubernetes](https://img.shields.io/badge/kubernetes-v1.28-326CE5?style=flat-square&logo=kubernetes)
![Jenkins](https://img.shields.io/badge/jenkins-v2.414-D24939?style=flat-square&logo=jenkins)
![SonarQube](https://img.shields.io/badge/sonarqube-v9.8-4E9BCD?style=flat-square&logo=sonarqube)
![Trivy](https://img.shields.io/badge/trivy-security%20scanner-1904DA?style=flat-square&logo=aqua)

</div>

## 🚀 Three-Tier Deployment Strategy

Our deployment strategy follows industry best practices with three distinct environments, each serving specific purposes in the software development lifecycle.

### 🛠️ **Development Environment**
- **Infrastructure**: AWS EC2 t3.medium instance
- **Purpose**: Local development and initial testing
- **Database**: Local MongoDB instance
- **Deployment**: Manual deployment via npm scripts
- **Access**: Developers only (VPN required)

```bash
Environment: Development
URL: http://dev-campground.internal:3000
Database: MongoDB (local instance)
Cache: Redis (local instance)
SSL: Self-signed certificates
```

### 🧪 **Staging Environment**
- **Infrastructure**: EKS cluster with 2 nodes (t3.small)
- **Purpose**: Integration testing, QA validation, and client demos
- **Database**: MongoDB Atlas (staging cluster)
- **Deployment**: Automated via Jenkins Pipeline 1
- **Access**: QA team, stakeholders, and developers

```bash
Environment: Staging
URL: https://staging-campground.yourdomain.com
Database: MongoDB Atlas (M10 cluster)
Cache: AWS ElastiCache Redis
SSL: Let's Encrypt certificates
Monitoring: Basic CloudWatch metrics
```

### 🏭 **Production Environment**
- **Infrastructure**: EKS cluster with 3 nodes (t3.medium) + Auto Scaling
- **Purpose**: Live application serving end users
- **Database**: MongoDB Atlas (production cluster with replica sets)
- **Deployment**: Automated via Jenkins Pipeline 2 with manual approval
- **Access**: End users and authorized administrators

```bash
Environment: Production
URL: https://campground.yourdomain.com
Database: MongoDB Atlas (M30 cluster with replica sets)
Cache: AWS ElastiCache Redis (cluster mode)
SSL: AWS Certificate Manager
Monitoring: Full observability stack (Prometheus + Grafana)
Backup: Daily automated backups
CDN: AWS CloudFront
```

### 🔄 **Environment Promotion Flow**

```
Development → Staging → Production
     ↓           ↓          ↓
   Manual     Automated   Automated
 Deployment  (Pipeline 1) (Pipeline 2)
               ↓          ↓
          Auto-triggered Manual Approval
          on PR merge   Required
```

## 🏗️ DevOps Architecture & CI/CD Pipeline

```mermaid
---
config:
  layout: dagre
---

flowchart TD
    %% 🎯 Dev Stage
    subgraph DEV_STAGE["🛠️ Dev Stage"]
        DEV["👨‍💻 Developer<br/>EC2 (t3.medium)"]
        GIT["📁 GitHub Repo"]
        DEV --> GIT
    end

    %% 🧱 CI/CD Core
    subgraph CICD["🧰 CI/CD Infrastructure"]
        JENKINS["🛠️ Jenkins<br/>EC2 (t3.large)"]
        SONAR["📊 SonarQube"]
        TRIVY["🛡️ Trivy - Image Scan"]
        GIT --> JENKINS
        JENKINS --> SONAR
        JENKINS --> TRIVY
    end

    %% 🧪 Staging Environment
    subgraph STAGE_ENV["🧪 Staging Environment"]
        STAGE_PIPE["🔁 Jenkins: Staging Pipeline"]
        ECR["📦 Push to ECR"]
        EKS_STAGE["☸️ EKS Cluster (Staging)"]
        STAGE_FE["🎨 Frontend Pod"]
        STAGE_BE["🔧 Backend Pod"]
        MONGO_STAGE["🗄️ MongoDB Atlas<br/>M10"]
        
        STAGE_PIPE --> ECR
        STAGE_PIPE --> EKS_STAGE
        EKS_STAGE --> STAGE_FE
        EKS_STAGE --> STAGE_BE
        STAGE_BE --> MONGO_STAGE
    end

    %% 🚀 Production Environment
    subgraph PROD_ENV["🏭 Production Environment"]
        PROD_PIPE["🚀 Jenkins: Production Pipeline"]
        PROD_DEPLOY["🌐 Deploy to EKS Prod (Manual Approval)"]
        EKS_PROD["☸️ EKS Cluster (Prod)<br/>3x t3.medium"]
        PROD_FE["🎨 Frontend Pods x2"]
        PROD_BE["🔧 Backend Pods x3"]
        MONGO_PROD["🗄️ MongoDB Atlas<br/>M30 RS"]
        ALB["🔗 AWS ALB"]


        PROD_PIPE --> PROD_DEPLOY
        PROD_DEPLOY --> EKS_PROD
        EKS_PROD --> PROD_FE
        EKS_PROD --> PROD_BE
        PROD_FE --> ALB
        PROD_BE --> ALB
        PROD_BE --> MONGO_PROD
    end

    %% 📦 Master Architecture Block
    subgraph ARCH["📦 Three-Tier CI/CD Architecture"]
        DEV_STAGE --> CICD --> STAGE_ENV --> PROD_ENV
    end
```

## 📋 Prerequisites

### 🛠️ **Required Software**
```bash
# Core Development Tools
Node.js >= 18.0.0
npm >= 8.0.0
Git >= 2.30.0
Docker >= 20.10.0
Docker Compose >= 2.0.0

# AWS Tools
AWS CLI v2
eksctl >= 0.147.0
kubectl >= 1.28.0
helm >= 3.12.0

# Optional but Recommended
k9s (Kubernetes CLI)
lens (Kubernetes IDE)
```

### ☁️ **AWS Prerequisites**
- AWS Account with billing enabled
- IAM user with programmatic access
- Required IAM permissions for EKS, EC2, S3, and CloudFormation
- AWS CLI configured with credentials

### 🏗️ **Infrastructure Requirements**
```yaml
Development EC2:
  Instance Type: t3.medium
  OS: Amazon Linux 2
  Storage: 30GB gp3
  Security Group: SSH (22), HTTP (3000, 5000)

Jenkins/SonarQube EC2:
  Instance Type: t3.large
  OS: Amazon Linux 2
  Storage: 50GB gp3
  Security Group: SSH (22), HTTP (8080, 9000)

EKS Staging Cluster:
  Node Type: t3.small
  Node Count: 2
  Auto Scaling: 1-3 nodes

EKS Production Cluster:
  Node Type: t3.medium
  Node Count: 3
  Auto Scaling: 2-5 nodes
```







