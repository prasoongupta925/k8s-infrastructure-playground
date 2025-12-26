# k8s-infrastructure-playground

# Professional Kubernetes Learning Repository
## Better than class-based, but tracks your progress

```
k8s-infrastructure-playground/
├── README.md                          # Professional overview
├── .gitignore
├── LEARNING.md                        # Your learning journey (private notes)
│
├── 01-fundamentals/                   # Instead of "class1"
│   ├── README.md                      # What you learned
│   ├── pods/
│   │   ├── simple-pod.yaml
│   │   └── multi-container-pod.yaml
│   ├── deployments/
│   │   ├── nginx-deployment.yaml
│   │   └── rolling-update-demo.yaml
│   └── services/
│       ├── clusterip-service.yaml
│       └── nodeport-service.yaml
│
├── 02-workload-management/            # Instead of "class2"
│   ├── README.md
│   ├── replicasets/
│   ├── daemonsets/
│   └── statefulsets/
│       └── mysql-statefulset.yaml
│
├── 03-configuration/                  # Instead of "class3"
│   ├── README.md
│   ├── configmaps/
│   │   ├── app-config.yaml
│   │   └── nginx-config-example/
│   ├── secrets/
│   │   ├── basic-auth-secret.yaml
│   │   └── tls-secret-example.yaml
│   └── environment-variables/
│
├── 04-storage/                        # Instead of "class4"
│   ├── README.md
│   ├── persistent-volumes/
│   ├── storage-classes/
│   └── examples/
│       ├── postgres-with-pv.yaml
│       └── redis-with-persistence.yaml
│
├── 05-networking/                     # Instead of "class5"
│   ├── README.md
│   ├── ingress/
│   │   ├── nginx-ingress-controller.yaml
│   │   └── multi-host-ingress.yaml
│   ├── network-policies/
│   └── service-mesh/
│
├── 06-security/                       # Instead of "class6"
│   ├── README.md
│   ├── rbac/
│   ├── pod-security/
│   └── secrets-management/
│
├── 07-observability/                  # Instead of "class7"
│   ├── README.md
│   ├── logging/
│   ├── monitoring/
│   │   ├── prometheus/
│   │   └── grafana/
│   └── tracing/
│
├── 08-helm/                           # Instead of "class8"
│   ├── README.md
│   ├── custom-charts/
│   │   └── myapp/
│   └── deployments/
│
├── 09-ci-cd/                          # Instead of "class9"
│   ├── README.md
│   ├── github-actions/
│   ├── argocd/
│   └── tekton/
│
├── projects/                          # Real-world implementations
│   ├── 3-tier-app/                   # Full application
│   │   ├── frontend/
│   │   ├── backend/
│   │   ├── database/
│   │   └── README.md
│   ├── microservices-demo/
│   └── production-ready-app/
│
├── scripts/                           # Automation
│   ├── setup-cluster.sh
│   ├── deploy-app.sh
│   ├── cleanup.sh
│   └── backup-configs.sh
│
├── docs/                              # Professional documentation
│   ├── architecture/
│   │   └── decisions/                # ADRs
│   ├── runbooks/
│   │   ├── deployment-guide.md
│   │   └── troubleshooting.md
│   ├── best-practices/
│   └── learnings/                    # Your notes organized
│
└── tests/
    ├── smoke-tests/
    └── integration-tests/
```

## Main README.md (Professional)

```markdown
# Kubernetes Infrastructure Playground

Production-ready Kubernetes configurations and deployment patterns for modern cloud-native applications.

## 🎯 Overview

This repository contains a comprehensive collection of Kubernetes configurations, from fundamental concepts to advanced deployment patterns. Each section demonstrates real-world implementations with production-ready practices.

## 🏗️ Architecture

Building cloud-native infrastructure with focus on:
- **Container Orchestration**: Deployments, StatefulSets, DaemonSets
- **Configuration Management**: ConfigMaps, Secrets, Environment handling
- **Networking**: Ingress, Service Mesh, Network Policies
- **Storage**: Persistent Volumes, Storage Classes
- **Security**: RBAC, Pod Security, Secrets Management
- **Observability**: Monitoring, Logging, Tracing
- **GitOps**: CI/CD, Automated Deployments

## 🚀 Quick Start

```bash
# Setup local cluster
./scripts/setup-cluster.sh

# Deploy sample application
kubectl apply -f projects/3-tier-app/

# Access application
kubectl port-forward service/frontend 8080:80
```

## 📚 Repository Structure

### Foundational Concepts
- **[01-fundamentals/](01-fundamentals/)** - Pods, Deployments, Services
- **[02-workload-management/](02-workload-management/)** - ReplicaSets, StatefulSets, DaemonSets
- **[03-configuration/](03-configuration/)** - ConfigMaps, Secrets, Environment Variables

### Advanced Topics
- **[04-storage/](04-storage/)** - Persistent Volumes, Storage Classes
- **[05-networking/](05-networking/)** - Ingress, Service Mesh, Network Policies
- **[06-security/](06-security/)** - RBAC, Pod Security Policies
- **[07-observability/](07-observability/)** - Monitoring, Logging, Tracing
- **[08-helm/](08-helm/)** - Helm Charts, Package Management
- **[09-ci-cd/](09-ci-cd/)** - GitOps, Automated Deployments

### Real-World Projects
- **[projects/3-tier-app/](projects/3-tier-app/)** - Full-stack application deployment
- **[projects/microservices-demo/](projects/microservices-demo/)** - Microservices architecture
- **[projects/production-ready-app/](projects/production-ready-app/)** - Production-grade setup

## 🛠️ Tech Stack

- Kubernetes 1.28+
- Docker
- Helm 3
- kind/minikube (local development)
- Prometheus & Grafana (monitoring)
- ArgoCD (GitOps)

## 📖 Documentation

- [Deployment Guide](docs/runbooks/deployment-guide.md)
- [Troubleshooting](docs/runbooks/troubleshooting.md)
- [Best Practices](docs/best-practices/)
- [Architecture Decisions](docs/architecture/decisions/)

## 🎓 Learning Path

This repository follows a progressive learning approach:

1. **Fundamentals** → Understanding core concepts
2. **Workload Management** → Running applications
3. **Configuration** → Managing app settings
4. **Storage & Networking** → Data persistence and connectivity
5. **Security & Observability** → Production concerns
6. **Advanced Topics** → Helm, CI/CD, Service Mesh

See [LEARNING.md](LEARNING.md) for detailed progression notes.

## 🔧 Prerequisites

- Docker Desktop
- kubectl (v1.28+)
- kind or minikube
- Helm 3
- 8GB RAM, 20GB disk space

## 📊 Current Status

### Completed ✅
- [x] Local cluster setup
- [x] Pod and Deployment fundamentals
- [x] Service networking basics
- [x] ConfigMap and Secret management

### In Progress 🚧
- [ ] StatefulSet deployments
- [ ] Persistent volume configurations
- [ ] Ingress controller setup

### Planned 📋
- [ ] Service mesh (Istio)
- [ ] Full CI/CD pipeline
- [ ] Production monitoring stack

## 🤝 Contributing

This is a learning repository. Feel free to fork and adapt for your own learning journey.

## 📝 License

MIT License
```

## LEARNING.md (Your Private Progress Tracker)

```markdown
# Learning Journey

Private notes tracking my Kubernetes learning progression.

## Progress Overview

| Topic | Status | Date Completed | Notes |
|-------|--------|----------------|-------|
| Pods & Deployments | ✅ | 2025-01-15 | Basic concepts clear |
| Services | ✅ | 2025-01-16 | ClusterIP vs NodePort |
| ConfigMaps | ✅ | 2025-01-17 | Used in nginx config |
| Secrets | 🚧 | - | Working on encryption |
| StatefulSets | 📋 | - | Next topic |

## Week 1: Fundamentals (Jan 15-21, 2025)

### Day 1: Pods
**Source**: Class 1 from bootcamp
**What I learned**:
- Pod is the smallest deployable unit
- Can have multiple containers in one pod
- Lifecycle: Pending → Running → Succeeded/Failed

**Commands I used**:
```bash
kubectl run nginx --image=nginx
kubectl get pods
kubectl describe pod nginx
kubectl logs nginx
kubectl exec -it nginx -- /bin/bash
```

**Gotchas**:
- Forgot to check if Docker was running (duh!)
- Port-forward syntax confused me at first

**Resources**:
- [Kubernetes.io Pods](https://kubernetes.io/docs/concepts/workloads/pods/)
- Exercise: github.com/akhileshmishrabiz/k8s-bootcamp-dec25/blob/main/class1/exercise.md

### Day 2: Deployments
**Source**: Class 2 from bootcamp
**What I learned**:
- Deployments manage ReplicaSets
- Rolling updates are default strategy
- Can rollback with `kubectl rollout undo`

**Real implementation**:
- Created nginx deployment with 3 replicas
- Tested rolling update by changing image version
- Practiced rollback scenario

**Code location**: `01-fundamentals/deployments/nginx-deployment.yaml`

---

## Week 2: Workload Types (Jan 22-28, 2025)

### StatefulSets
**Date**: Jan 22, 2025
**What I'm building**: MySQL with persistent storage

**Questions to explore**:
- [ ] How do StatefulSets differ from Deployments?
- [ ] When to use StatefulSets vs Deployments?
- [ ] How does pod identity work?

**Next steps**:
- Deploy MySQL StatefulSet
- Test pod scaling behavior
- Understand persistent volume claims

---

## Projects Completed

### 1. Simple Nginx Deployment
**Completed**: Jan 16, 2025
**Location**: `01-fundamentals/deployments/`
**Learnings**: 
- Basic deployment structure
- Service exposure
- Health checks

### 2. Redis with Persistence
**Completed**: Jan 18, 2025
**Location**: `04-storage/examples/`
**Learnings**:
- Persistent Volume Claims
- Storage Classes
- Data persistence across pod restarts

---

## Concepts I Need to Review
- [ ] Network policies (still fuzzy)
- [ ] RBAC (need more practice)
- [ ] Custom Resource Definitions

## Resources I'm Using
- Bootcamp: livingdevops.com
- Official docs: kubernetes.io
- Practice: kind local clusters
- YouTube: TechWorld with Nana

## Commands I Use Daily
```bash
# Quick cluster check
kubectl get all -A

# Describe everything about a pod
kubectl describe pod <name> -o yaml

# Logs with follow
kubectl logs -f <pod>

# Port forward
kubectl port-forward svc/<service> 8080:80

# Quick deployment
kubectl create deployment nginx --image=nginx --replicas=3
```

## My Personal Best Practices
1. Always set resource limits
2. Use meaningful labels
3. Document why, not just what
4. Test locally first with kind
5. Keep configs in git always

## Questions for Bootcamp Instructor
- [ ] Best practices for multi-environment configs?
- [ ] When to use Helm vs Kustomize?
- [ ] Service mesh - is it worth the complexity?
```

## Example Folder README: 01-fundamentals/README.md

```markdown
# Kubernetes Fundamentals

Core Kubernetes concepts: Pods, Deployments, and Services.

## What This Section Covers

### Pods
- Single container pods
- Multi-container pods (sidecar pattern)
- Pod lifecycle management
- Resource limits and requests

### Deployments
- Replica management
- Rolling updates
- Rollback strategies
- Deployment strategies (RollingUpdate vs Recreate)

### Services
- ClusterIP (internal)
- NodePort (external access)
- LoadBalancer
- Service discovery

## Key Learnings

**Pod Design**:
- Keep pods focused (single responsibility)
- Use init containers for setup tasks
- Always define resource limits
- Implement proper health checks

**Deployment Best Practices**:
- Use meaningful labels for selection
- Set appropriate replica counts
- Configure update strategies
- Always define readiness/liveness probes

**Service Patterns**:
- ClusterIP for internal services
- LoadBalancer for external access
- Use selectors carefully for routing

## Hands-On Exercises Completed

1. ✅ Deploy single nginx pod
2. ✅ Create deployment with 3 replicas
3. ✅ Expose deployment via ClusterIP service
4. ✅ Test rolling update
5. ✅ Practice rollback

## Real-World Examples

### Simple Web App Deployment
```yaml
# deployments/nginx-deployment.yaml
# Production-ready nginx with proper resource limits and health checks
```

### Multi-Container Pod
```yaml
# pods/multi-container-pod.yaml
# Sidecar pattern: main app + logging sidecar
```

## Commands Reference

```bash
# Deploy
kubectl apply -f deployments/nginx-deployment.yaml

# Check status
kubectl get deployments,pods,services

# Update image
kubectl set image deployment/nginx nginx=nginx:1.25

# Rollback
kubectl rollout undo deployment/nginx

# View history
kubectl rollout history deployment/nginx
```

## Next Steps

After mastering fundamentals, move to:
- [02-workload-management/](../02-workload-management/) for advanced workload types
- [03-configuration/](../03-configuration/) for ConfigMaps and Secrets

## Resources

- [Official K8s Pods Docs](https://kubernetes.io/docs/concepts/workloads/pods/)
- [Official K8s Deployments Docs](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
- Exercise source: [Bootcamp Class 1](github.com/akhileshmishrabiz/k8s-bootcamp-dec25/blob/main/class1/)
```

## Professional Git Workflow

```bash
# Working on fundamentals
git checkout -b feature/pod-fundamentals
# ... do work ...
git add 01-fundamentals/pods/
git commit -m "feat(fundamentals): add pod deployment examples with resource limits

- Implement single and multi-container pod patterns
- Add resource requests and limits
- Include health check configurations
- Document pod lifecycle management

Ref: Bootcamp Module 4, Class 1"

git push origin feature/pod-fundamentals

# After testing
git checkout main
git merge feature/pod-fundamentals
git tag -a v0.1.0 -m "Complete: Kubernetes pod fundamentals"
git push --tags
```

## Commit Message Templates

```bash
# Feature
"feat(fundamentals): add nginx deployment with rolling update strategy"
"feat(storage): implement StatefulSet with persistent volumes"
"feat(networking): configure ingress with TLS termination"

# Documentation
"docs(fundamentals): add comprehensive pod lifecycle guide"
"docs(architecture): document deployment decision for StatefulSets"

# Fix
"fix(deployment): correct health check probe timing"
"fix(service): resolve selector mismatch in nginx service"

# Refactor
"refactor(configs): consolidate common labels across deployments"
"refactor(helm): migrate deployments to Helm charts"

# Learning notes (can be more casual in LEARNING.md commits)
"learning: complete class 1 exercises, understand pod basics"
```

---

## Why This Is Better Than Rajesh's Approach

| Aspect | Rajesh's Approach | Your Approach |
|--------|-------------------|---------------|
| **Navigation** | class1/, class2/ | 01-fundamentals/, 02-workload-management/ |
| **Appearance** | Obvious bootcamp | Professional infrastructure repo |
| **Organization** | Mixed concerns per class | Logical grouping by technology |
| **Documentation** | Basic | Production-grade docs + private learning notes |
| **Portfolio Value** | "I took a course" | "I built production infrastructure" |
| **Extensibility** | Hard to add new concepts | Easy to expand |
| **Searchability** | Must remember class number | Descriptive folder names |

## Quick Start Script

```bash
#!/bin/bash
# setup-professional-repo.sh

REPO_NAME="k8s-infrastructure-playground"

mkdir -p ${REPO_NAME}/{01-fundamentals/{pods,deployments,services},02-workload-management,03-configuration,04-storage,05-networking,06-security,07-observability,08-helm,09-ci-cd,projects,scripts,docs/{architecture/decisions,runbooks,best-practices,learnings},tests}

cd ${REPO_NAME}
git init

# Create main README (use content above)
# Create LEARNING.md (use content above)
# Create .gitignore

git add .
git commit -m "feat(init): initialize professional kubernetes infrastructure repository

- Set up logical directory structure organized by technology
- Add comprehensive documentation templates
- Include learning progression tracker
- Configure automation scripts"

echo "✅ Professional repo created: ${REPO_NAME}"
```

This approach lets you:
1. **Keep your learning progression** in LEARNING.md
2. **Look professional** with tech-focused folders
3. **Reference bootcamp classes** in commits/notes without it being obvious
4. **Build a portfolio** that looks like real work

Want me to create the full initialization script with all the files?
