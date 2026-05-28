# homelab-gitops

Background story for this repository is that this is not a live gitops repository,
but instead it is how I would build things if I would have to build new k3s from scratch.

## Roadmap

In higher level story is:
1. bootstrap fluxcd
2. add traefik and cert-manager
3. add rustfs as we will need something that works like AWS S3
4. add longhorn to work as file system
5. add cnpg-postgresql as we will need postgresql for bunch of services
6. add forgejo as first real service
7. add kube-prometheus-stack to give us view on how k3s is working

## TODO or things that we've done manually
- secrets are create outside of fluxcd
  - cloudflare's api token for cert-manager
- buckets have been done with rustfs UI
  - one for longhorn
  - one for each cnpg cluster
- longhorn backups have been defined in longhorn UI
  - backup forgejo's pvc:wq
- grafana dashboards have been done in grafana UI
