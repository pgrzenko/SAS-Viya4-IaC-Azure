# Azure Infrastructure as Code (IaC) – Modular Terraform Templates

This repository contains a modular and production-ready set of Terraform templates to provision Azure infrastructure. Originally based on enterprise deployment patterns, this framework provides a scalable foundation for any cloud-native solution deployed in Azure – whether analytical workloads, container platforms, or custom applications.

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Managing Resources](#managing-resources)
- [Security](#security)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Overview

This framework provisions Azure infrastructure components including:

- Resource groups
- Virtual networks, subnets, NSGs and rules
- Azure Kubernetes Service (AKS)
- User and system node pools with taints and labels
- Optional PostgreSQL DB
- Azure Container Registry
- Storage (NFS or Azure NetApp Files)
- Diagnostics, logging and monitoring integrations

All components are built with modularity, reusability, and automation in mind.

> This repository does **not** require or reference any vendor-specific software stack. Use it as a standalone infrastructure blueprint.

## Prerequisites

- Terraform >= 1.4  
- Azure CLI  
- `kubectl`  
- `jq`  
- Docker (optional, for isolated Terraform runs)  
- An Azure subscription and contributor-level identity

## Getting Started

```bash
git clone https://github.com/pgrzenko/SAS-Viya4-IaC-Azure.git
cd SAS-Viya4-IaC-Azure

# Authenticate to Azure
az login

# Initialize Terraform
terraform init
terraform plan
terraform apply
```
