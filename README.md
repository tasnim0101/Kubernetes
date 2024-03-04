# Apply
# Node exporter
```sh
kubectl apply -f node-exporter
kubectl get endpoints
# Access node exporter
http://192.168.43.222:30910/
```
# Prometheus 
## Role for prometheus access to kubernetes resources
```sh
kubectl apply -f prometheus-role-management
# Get service account
kubectl get sa
```
# Prometheus resources
```sh
kubectl apply -f prometheus-resources
# Visit prometheus url
http://192.168.43.222:30990
```

# Grafana resources
```sh
kubectl apply -f grafana-resources
# Visit grafana url
http://192.168.43.222:30300
```



# Grafana dashboards 
- all dashboards: https://grafana.com/grafana/dashboards/
- node monitoring: https://grafana.com/grafana/dashboards/8171-kubernetes-nodes/


# Destroy all
```sh
kubectl delete -f node-exporter
kubectl delete -f prometheus-role-management
kubectl delete -f prometheus-resources
kubectl delete -f grafana-resources
```
# Apply all
```sh
kubectl apply -f node-exporter
kubectl apply -f prometheus-role-management
kubectl apply -f prometheus-resources
kubectl apply -f grafana-resources
```
