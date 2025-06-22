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

### **Frontend Technologies**
![React](https://img.shields.io/badge/react-v18.2.0-61DAFB?style=flat-square&logo=react)
![TypeScript](https://img.shields.io/badge/typescript-v4.9.4-3178C6?style=flat-square&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/tailwindcss-v3.2.4-06B6D4?style=flat-square&logo=tailwindcss)
![Vite](https://img.shields.io/badge/vite-v4.0.0-646CFF?style=flat-square&logo=vite)

### **Backend Technologies**
![Node.js](https://img.shields.io/badge/node.js-v18.12.1-339933?style=flat-square&logo=node.js)
![Express](https://img.shields.io/badge/express-v4.18.2-000000?style=flat-square&logo=express)
![MongoDB](https://img.shields.io/badge/mongodb-v6.0-47A248?style=flat-square&logo=mongodb)
![Redis](https://img.shields.io/badge/redis-v7.0-DC382D?style=flat-square&logo=redis)

### **DevOps & Cloud**
![AWS](https://img.shields.io/badge/AWS-EKS%20%7C%20EC2%20%7C%20S3-FF9900?style=flat-square&logo=amazon-aws)
![Docker](https://img.shields.io/badge/docker-v20.10-2496ED?style=flat-square&logo=docker)
![Kubernetes](https://img.shields.io/badge/kubernetes-v1.28-326CE5?style=flat-square&logo=kubernetes)
![Jenkins](https://img.shields.io/badge/jenkins-v2.414-D24939?style=flat-square&logo=jenkins)

### **Code Quality & Security**
![SonarQube](https://img.shields.io/badge/sonarqube-v9.8-4E9BCD?style=flat-square&logo=sonarqube)
![Trivy](https://img.shields.io/badge/trivy-security%20scanner-1904DA?style=flat-square&logo=aqua)
![OWASP](https://img.shields.io/badge/OWASP-ZAP-000000?style=flat-square&logo=owasp)

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



### 🌐 **Access Points**
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:5000/api/v1
- **API Documentation**: http://localhost:5000/api-docs
- **GraphQL Playground**: http://localhost:5000/graphql



graph TB
    %% Developer Workflow
    DEV[👨‍💻 Developer] --> GIT[📁 GitHub Repository]
    GIT --> |Push to develop| JENKINS[🔧 Jenkins<br/>Port 8080]
    GIT --> |PR to main| JENKINS
    GIT --> |Merge to main| JENKINS

    %% Development Environment
    subgraph DEV_ENV[🛠️ Development Environment]
        EC2_DEV[🖥️ EC2 Instance<br/>t3.medium]
        MONGO_DEV[🗄️ MongoDB Local]
        
        EC2_DEV --> MONGO_DEV
    end

    %% CI/CD Infrastructure
    subgraph CICD_INFRA[🏗️ CI/CD Infrastructure]
        EC2_JENKINS[🖥️ EC2 Instance<br/>t3.large]
        JENKINS
        SONAR[📊 SonarQube<br/>Port 9000]
        
        EC2_JENKINS --> JENKINS
        EC2_JENKINS --> SONAR
    end

    %% Pipeline 1 - Staging
    subgraph PIPELINE1[🔄 Pipeline 1: Staging]
        P1_CHECKOUT[📥 Checkout Code]
        P1_DEPS[📦 Install Dependencies]
        P1_TEST[🧪 Run Tests<br/>Coverage: 80%+]
        P1_SONAR[📊 SonarQube Analysis<br/>Quality Gates]
        P1_SECURITY[🔒 Security Scan<br/>OWASP + npm audit]
        P1_BUILD[🐳 Build Docker Images]
        P1_TRIVY[🛡️ Trivy Security Scan<br/>HIGH/CRITICAL]
        P1_DEPLOY_STAGING[🚀 Deploy to Staging]
        
        P1_CHECKOUT --> P1_DEPS
        P1_DEPS --> P1_TEST
        P1_TEST --> P1_SONAR
        P1_SONAR --> P1_SECURITY
        P1_SECURITY --> P1_BUILD
        P1_BUILD --> P1_TRIVY
        P1_TRIVY --> P1_DEPLOY_STAGING
    end

    %% Pipeline 2 - Production
    subgraph PIPELINE2[🔄 Pipeline 2: Production]
        P2_VALIDATE[✅ Pre-deployment Validation]
        P2_SECURITY[🔐 Final Security Check]
        P2_BUILD[🏗️ Production Build]
        P2_APPROVAL[👥 Manual Approval<br/>DevOps Lead + PO]
        P2_DEPLOY[🌐 Blue-Green Deploy<br/>Zero Downtime]
        P2_HEALTH[🔍 Health Checks]
        P2_NOTIFY[📧 Email Notification]
        
        P2_VALIDATE --> P2_SECURITY
        P2_SECURITY --> P2_BUILD
        P2_BUILD --> P2_APPROVAL
        P2_APPROVAL --> P2_DEPLOY
        P2_DEPLOY --> P2_HEALTH
        P2_HEALTH --> P2_NOTIFY
    end

    %% Staging Environment
    subgraph STAGING_ENV[🧪 Staging Environment]
        EKS_STAGING[☸️ EKS Cluster<br/>2 x t3.small nodes]
        MONGO_ATLAS_STAGING[🗄️ MongoDB Atlas<br/>M10 Cluster]
        
        subgraph STAGING_PODS[Staging Pods]
            BACKEND_STAGING[🔧 Backend Pod<br/>campground-backend]
            FRONTEND_STAGING[🎨 Frontend Pod<br/>campground-frontend]
        end
        
        EKS_STAGING --> STAGING_PODS
        BACKEND_STAGING --> MONGO_ATLAS_STAGING
    end

    %% Production Environment
    subgraph PROD_ENV[🏭 Production Environment]
        EKS_PROD[☸️ EKS Cluster<br/>3 x t3.medium nodes<br/>Auto Scaling: 2-5]
        MONGO_ATLAS_PROD[🗄️ MongoDB Atlas<br/>M30 Cluster + Replica Sets]
        
        subgraph PROD_PODS[Production Pods]
            BACKEND_PROD[🔧 Backend Pods<br/>3 replicas]
            FRONTEND_PROD[🎨 Frontend Pods<br/>2 replicas]
        end
        
        subgraph PROD_SERVICES[Production Services]
            ALB[🔗 AWS Load Balancer]
            CLOUDFRONT[🌐 CloudFront CDN]
            ACM[🔒 SSL Certificate<br/>AWS Certificate Manager]
        end
        
        EKS_PROD --> PROD_PODS
        BACKEND_PROD --> MONGO_ATLAS_PROD
        CLOUDFRONT --> ALB
        ALB --> FRONTEND_PROD
        ALB --> BACKEND_PROD
        ACM --> ALB
    end

    %% External Services
    subgraph EXTERNAL[🌐 External Services]
        USERS[👥 End Users]
        ECR[📦 AWS ECR<br/>Container Registry]
    end

    %% Connections
    JENKINS --> PIPELINE1
    JENKINS --> PIPELINE2
    
    PIPELINE1 --> STAGING_ENV
    PIPELINE2 --> PROD_ENV
    
    P1_BUILD --> ECR
    P2_BUILD --> ECR
    ECR --> EKS_STAGING
    ECR --> EKS_PROD
    
    USERS --> CLOUDFRONT
    
    %% Styling
    classDef devEnv fill:#e1f5fe,stroke:#01579b,stroke-width:2px
    classDef stagingEnv fill:#f3e5f5,stroke:#4a148c,stroke-width:2px
    classDef prodEnv fill:#e8f5e8,stroke:#1b5e20,stroke-width:2px
    classDef cicdEnv fill:#fff3e0,stroke:#e65100,stroke-width:2px
    classDef external fill:#fafafa,stroke:#424242,stroke-width:2px
    
    class DEV_ENV devEnv
    class STAGING_ENV stagingEnv
    class PROD_ENV prodEnv
    class CICD_INFRA,PIPELINE1,PIPELINE2 cicdEnv
    class EXTERNAL external




**⭐ If you found this project helpful, please give it a star! ⭐**

![GitHub stars](https://img.shields.io/github/stars/yourusername/camp-ground?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/camp-ground?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/yourusername/camp-ground?style=social)

Made with ❤️ by [Your Name](https://github.com/yourusername)

</div>




