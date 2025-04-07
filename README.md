# ArgoCD + OpenShift + Nvidia H100 MIG + Neural Magic vLLM Demo

This repo demonstrates how to maximize GPU utilization on OpenShift with:

🚀 **Nvidia H100 + MIG** for GPU partitioning and multi-tenancy  
🧠 **Neural Magic (vLLM)** for optimized LLM inference  
🛠️ **Ansible** for automation  
📦 **ArgoCD** for GitOps-based deployment

## What’s Inside?

- `ansible/roles/mig_config`: Enables MIG mode and slices the H100 into 7 x `1g.10gb` profiles.
- `k8s/migconfig`: MIGConfig CR to automate GPU partitioning using Nvidia MIG Manager.
- `k8s/vllm`: Pod manifest to deploy vLLM optimized inference on MIG instances.
- `argocd/application.yaml`: ArgoCD `Application` to deploy everything GitOps-style.

## Quick Start

1. Enable ArgoCD and apply `argocd/application.yaml`.
2. Run the Ansible role to enable MIG on GPU nodes.
3. Watch OpenShift do its magic with MIG + vLLM!

Built for teams that want **max performance-per-dollar** on OpenShift GPUs.  
