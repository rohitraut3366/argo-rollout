# argo-rollout

Flow:
## Before New release
```
pod:
  stable:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=59cbf449cc
  canary:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=59cbf449cc

svc:
  stable:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=59cbf449cc
  canary:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=59cbf449cc

```
## After New Release:
```
pod:
  stable:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=59cbf449cc
  canary:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=6954649cdb

svc:
  stable:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=59cbf449cc
  canary:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=6954649cdb
```

## After Analysis completed
```
pod:
  stable:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=6954649cdb
  canary:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=6954649cdb

svc:
  stable:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=6954649cdb
  canary:
        app.kubernetes.io/instance=app-test
        app.kubernetes.io/name=poc-argorollout
        rollouts-pod-template-hash=6954649cdb

```