# infra-k3s

Infrastructure GitOps pour mon cluster K3s (VPS OVH) pilotée par Argo CD.

Ce repo ne contient **que l’infra** et la glue GitOps :
- Argo CD (ingress, metrics…)
- cert-manager (Let’s Encrypt)
- stack de monitoring (kube-prometheus-stack + Grafana)
- namespaces applicatifs
- AppProjects Argo CD

---

## 🧱 Structure du repo

```text
infra-k3s/
├── README.md
└── apps/
    ├── argocd/
    │   ├── ingress.yaml
    │   └── servicemonitors.yaml
    ├── cert-manager/
    │   └── clusterissuer-letsencrypt.yaml
    ├── monitoring/
    │   └── app-kube-prometheus-stack.yaml
    ├── namespaces/
    │   └── ns-babeau-website.yaml
    └── projects/
    └── project-babeau-website.yaml