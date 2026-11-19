# MLOps Assignment

Kubernetes and Git workflow assignment (MLOps, CS02125).

## What this project contains
- `nginx-pod.yaml`: Pod running an nginx container (label `app: nginx`)
- `nginx-service.yaml`: NodePort Service that routes traffic to the pod using the same label
- `app.yml`: application config
- `requirements.txt`: Python dependencies with pinned versions

## How to run
1. Start the cluster: `minikube start --driver=docker`
2. Deploy: `kubectl apply -f nginx-pod.yaml -f nginx-service.yaml`
3. Check: `kubectl get pods` and `kubectl get svc`
4. Open: `minikube service nginx-service --url`

## Git workflow used
main -> feature branch -> commit -> push -> pull request -> merge
