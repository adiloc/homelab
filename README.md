# Homelab GitOps Repository Structure

homelab/
├── clusters/
│   └── k3s/                # Your K3s cluster
│       ├── apps/                # Apps grouped by function
│       │   ├── networking/      # WireGuard, Traefik
│       │   ├── monitoring/      # Prometheus, Grafana
│       │   ├── services/        # Homepage, Nextcloud
│       │   └── kustomization.yaml  # Auto-discovers apps
│       ├── infrastructure/      # Cluster-wide tools
│       │   ├── cert-manager/
│       │   ├── metallb/
│       │   └── kustomization.yaml
│       └── flux-system/         # Flux bootstrap (auto-generated)
│
├── base/                        # Reusable components
│   ├── namespaces/
│   │   ├── networking.yaml
│   │   └── services.yaml
│   └── crds/                    # Custom Resource Definitions
│
├── app-sources/                 # Helm/OCI sources
│   ├── wireguard/
│   └── homepage/
│
├── .sops.yaml                   # SOPS encryption config
└── README.md                    # Setup guide
