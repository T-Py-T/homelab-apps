# 🚀 Homelab Applications - Self-Hosted Services

> **Production-ready self-hosted applications** - Deploy Homepage dashboard, n8n automation, RSS reader, bookmark manager, and read-later service with full security and monitoring integration.

---

## 📖 Overview

This repository contains **end-user applications** that run on the homelab platform. Automatically deployed by ArgoCD after platform and monitoring services are ready, providing a complete suite of self-hosted productivity and automation tools with enterprise-grade security and observability.

### 🎯 Repository Purpose

- Deploy self-hosted applications with GitOps automation
- Integrate applications with platform services (Vault, Keycloak, Istio)
- Provide production-ready configurations with monitoring
- Enable secure external access through service mesh
- Implement backup and disaster recovery for application data

---

## 🏗️ Repository Structure

homelab-apps/
├── environments/                    # Environment-specific configurations
│   ├── dev/
│   │   ├── external-secrets/       # Vault secret synchronization
│   │   │   ├── commafeed-secret.yaml
│   │   │   ├── homepage-secret.yaml
│   │   │   ├── linkding-secret.yaml
│   │   │   ├── n8n-secret.yaml
│   │   │   ├── postgresql-secret.yaml
│   │   │   ├── redis-secret.yaml
│   │   │   └── wallabag-secret.yaml
│   │   ├── istio-virtual-service.yaml  # Service mesh routing
│   │   ├── namespaces.yaml          # Application namespaces
│   │   ├── kustomization.yaml       # Environment kustomization
│   │   └── values/                  # Helm values for applications
│   │       ├── values-commafeed.yaml
│   │       ├── values-homepage.yaml
│   │       ├── values-linkding.yaml
│   │       ├── values-n8n.yaml
│   │       ├── values-postgresql.yaml
│   │       ├── values-redis.yaml
│   │       └── values-wallabag.yaml
│   ├── staging/                     # Staging environment configs
│   └── prod/                       # Production environment configs
└── docs/                           # Documentation

---

## 🚀 Deployed Applications

### 🏠 Homepage Dashboard

- **Purpose**: Centralized portal for homelab services
- **Access**: `homepage.dev.cluster.local`
- **Features**: Service status monitoring, quick access links

### 🔄 n8n Workflow Automation

- **Purpose**: Automate tasks and integrate services
- **Access**: `n8n.dev.cluster.local`
- **Features**: Visual workflow builder, 300+ integrations

### 📰 Commafeed RSS Reader

- **Purpose**: Self-hosted RSS feed aggregation
- **Access**: `commafeed.dev.cluster.local`
- **Features**: Clean interface, OPML import/export

### 🔖 Linkding Bookmark Manager

- **Purpose**: Organize and search bookmarks
- **Access**: `linkding.dev.cluster.local`
- **Features**: Tagging system, full-text search

### 📚 Wallabag Read Later

- **Purpose**: Save articles for offline reading
- **Access**: `wallabag.dev.cluster.local`
- **Features**: Full-text extraction, mobile apps