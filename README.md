## BEST PRACTICE (Industry Standard)

👉 Do NOT write Prometheus & Grafana YAML manually
👉 Use kube-prometheus-stack Helm chart

## Update Project Structure

realtime-project/

├── Chart.yaml

├── values.yaml

├── charts/

│   └── kube-prometheus-stack/

├── templates/

│   ├── servicemonitor.yaml

│   └── grafana-ingress.yaml



# Install / Upgrade Helm Chart
```
helm dependency update realtime-project
helm upgrade --install realtime-project ./realtime-project \
  -n realtime-prod --create-namespace
  ```

## Access Grafana
```
kubectl get ingress -n realtime-prod
```

Login:

Username: admin

Password: admin123

