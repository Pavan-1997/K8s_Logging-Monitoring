# K8s_Logging-Monitoring

![image](https://github.com/user-attachments/assets/a7643b81-3625-4f61-8ab0-32660110f517)

1. Install Metrics server
```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

2. Edit the Metric server deployment to disable certificate validation
```
k edit deploy metrics-server -n kube-system
```
Pass the argument `--kubelet-insecure-tls` as below

![image](https://github.com/user-attachments/assets/46549e68-840a-4be4-a50f-84dc2a687041)

3. Check the metrics server
```
k top node
```

![image](https://github.com/user-attachments/assets/02c6f62b-802d-47d7-924d-20ccee190c97)
