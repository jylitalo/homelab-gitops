# homelab-gitops

Background story for this repository is that this is not a live gitops repository,
but instead it is how I would build things if I would have to build new k3s from scratch.

## Roadmap

In higher level story is:
1. bootstrap fluxcd
2. add [traefik](https://github.com/traefik/traefik) and [cert-manager](https://github.com/cert-manager/cert-manager)
3. add [longhorn](https://github.com/longhorn/longhorn) to work as file system
4. add [rustfs](https://github.com/rustfs/rustfs) as we will need something that works like AWS S3 (uses longhorn for storage)
5. add [cnpg-postgresql](https://github.com/cloudnative-pg/cloudnative-pg) as we will need postgresql for bunch of services
6. add [forgejo](https://codeberg.org/forgejo/forgejo) as first real service
7. add [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack) to give us view on how k3s is working
8. add [immich](https://github.com/immich-app/immich)

## TODO or things that we've done manually
- secrets are create outside of fluxcd
  - cloudflare's api token for cert-manager
  - access keypair(s) for using rustfs
- rustfs buckets have been done with rustfs UI
  - one for longhorn
  - one for each cnpg cluster
- longhorn backups have been defined in longhorn UI
  - backup forgejo's pvc
- grafana dashboards have been done in grafana UI
