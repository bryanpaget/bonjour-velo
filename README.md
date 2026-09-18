# Bonjour Velo

Bonjour Velo is a realistic national bike-share platform mockup for **Digital Transformations Canada**, the fictional government IT agency. It is an on-brand, deployable example of a city-scale bikeshare system: static product page served from GitHub Pages, and the entire operational fleet defined as Kubernetes manifests.

The joke (if you squint): *the bikes are free to take*. The product page leans into it gently — the locks are psychological, the pricing is cheap, and the fleet is on Kubernetes.

## What's inside

| Path | Purpose |
| --- | --- |
| `docs/index.html` | Static product / landing page, hosted on GitHub Pages |
| `k8s/` | National fleet defined as Kubernetes YAML (kustomize) |
| `.github/workflows/pages.yml` | Build + deploy Pages site on push to `main` |
| `.github/workflows/validate-k8s.yml` | Client-side validation of all manifests in CI |
| `Makefile` | One-command setup, validate, deploy |
| `README.md` | This file |

## Pricing (cheap, by decree)

| Class | Per 15 min | Own it outright |
| --- | --- | --- |
| Mil-Spec Standard | $0.50 | $249.99 |
| Mil-Spec E-Assist | $0.50 | $399.99 |
| Mil-Spec Cargo Quad | $0.50 | $599.99 |

Like a bike? **Keep it.** File Form CSB-42 and it's yours. No lock required (the lock is psychological).

## Quick start

```bash
make setup       # initialize
make validate    # client-side check of the k8s manifests (works without a cluster)
make deploy      # kubectl apply -k k8s
make undeploy    # kubectl delete -k k8s
```

## License

GPL-3.0. Like the bikes, this repo is free to take.
# bonjour-velo
