# onboarding-platform

A tiny platform: a client contract, a composition
and a loop that keeps it true. Flux + Crossplane v2 on kind.

- `platform/`: the contract (XRD), the recipe (Composition in
  Python), the function package and RBAC. A `Client` is cluster-scoped
  and creates its own namespace `<environment>-<name>`.
- Client contracts live in a separate repo,
  [onboarding-clients](https://github.com/RalphieKay/onboarding-clients).
  Teams write there and never touch this one.
- `infrastructure/`: Crossplane itself, installed by Flux.
- `flux/`: applied once by hand to connect the cluster to both repos.
- `examples/`: files for experiments (invalid contracts, an app).

Everything runs locally. No cloud account needed.
