
<p align="center">
    <img src="https://raw.githubusercontent.com/kubernetes/kubernetes/master/logo/logo.png" alt="Kubernetes" height="60">
</p>

# webapp

A Helm chart for deploying webapp

## Project Structure
```
├── Chart.yaml
├── README.md
├── templates
│   ├── _helpers.tpl
│   ├── deployment.yaml
│   ├── pv.yaml
│   ├── pvc.yaml
│   └── service.yaml
├── values.yaml
└── webapp-0.0.1.tgz
```

## Prerequisites

- K3s/K8s cluster
- Helm 3.2.0+

## Installing the Chart

```bash
kubectl create namespace webapp
helm install webapp . --namespace webapp
```

This will:
- Create the `webapp` namespace (if not present)
- Apply the PV, PVC, ConfigMap, Deployment, and Service resources 

### 3. Access the Web Application

The service is exposed on NodePort `31234`. You can access it at:

```
http://localhost:31234/ in web browser or test with - curl localhost:31234
```

Author:
- Dmitri Donskoy
- Email: crooper22@gmail.com

## License

MIT License