# Gatekeeper Demo

## Installation

Install Gatekeeper via Helm

```bash
helm repo add gatekeeper https://open-policy-agent.github.io/gatekeeper/charts
helm install gatekeeper/gatekeeper --name-template=gatekeeper \
  --namespace gatekeeper-system \
  --create-namespace
```

## Usage

Deploy templates and constraints

```bash
kubectl apply -f policies/templates
kubectl apply -f policies/constraints
```

Deploy mutations

```bash
kubectl apply -f mutations
```

Deploy resources

```bash
kubectl apply -f resources --recursive
```


## References

[OPA Gatekeeper Library](https://github.com/open-policy-agent/gatekeeper-library)