repo/
├── .github/
│   └── workflows/
│       ├── ci.yml                  # tests y lint en PR
│       ├── security.yml            # escaneo de vulnerabilidades
│       ├── release.yml             # versionado semántico automático
│       ├── terraform.yml           # plan en PR, apply en merge
│       ├── ansible.yml             # mantenimiento manual de VPS
│       ├── notify.yml              # reporte semanal a Slack
│       ├── cleanup.yml             # limpieza de branches e imágenes
│       ├── stale.yml               # cerrar issues y PRs inactivos
│       ├── deploy-staging.yml      # deploy a staging en PR
│       └── deploy-production.yml   # deploy a producción en merge
├── helm/
│   └── app/
│       ├── Chart.yaml
│       ├── values.yaml
│       ├── values.staging.yaml
│       ├── values.production.yaml
│       └── templates/
│           ├── deployment.yaml
│           ├── service.yaml
│           └── ingress.yaml
├── infra/                        # opentofu
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── modules/
│       ├── vultr/
│       ├── cloudflare/
│       └── aws/
├── playbooks/                    # ansible
│   ├── restart.yml
│   ├── update.yml
│   └── inventory/
│       ├── hosts.yml
│       └── group_vars/
│           └── all.yml
├── public/                       # sitio estático
│   ├── index.html
│   ├── css/
│   └── js/
├── Dockerfile
├── compose.yaml
├── compose.override.yaml.example   # plantilla para devs
└── .gitignore                      # ignora compose.override.yaml

