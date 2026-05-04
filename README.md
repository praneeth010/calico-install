# 🚀 Calico Installation Guide (Kubernetes)

This guide explains how to install Calico CNI on a Kubernetes cluster using different datastore options.

🔗 Official Documentation:  
https://calico-v3-25.netlify.app/archive/v3.25/getting-started/kubernetes/self-managed-onprem/onpremises

---

## 📌 Prerequisites

- Kubernetes cluster (initialized using `kubeadm` or similar)
- `kubectl` configured and working
- Root or sudo access
- Pod network CIDR should match Calico (default: `192.168.0.0/16`)

---

## 🧩 Installation Options

Choose the appropriate installation method based on your cluster size and requirements.

---

### 1️⃣ Kubernetes API Datastore (≤ 50 Nodes) ✅ Recommended

Best for small to medium clusters.

```bash
curl https://raw.githubusercontent.com/projectcalico/calico/v3.25.0/manifests/calico.yaml -o calico.yaml

kubectl apply -f calico.yaml

curl https://raw.githubusercontent.com/projectcalico/calico/v3.25.0/manifests/calico-typha.yaml -o calico.yaml

kubectl apply -f calico.yaml


<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2532198e-6f2b-4421-913a-d4bae87850b0" />
