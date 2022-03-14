## Build Container Image for Grafana Reporter

```bash
docker build -t my-docker-hub.io/grafana-reporter:latest .
docker push my-docker-hub.io/grafana-reporter:latest 
```

## Deploy Grafana Reporter onto K8s

```bash
kubectl apply -f ./*.yaml
```  

### Configure Grafana Dashboard

Add a link to Grafana dashboard.

```bash
https://grafana-reporter.wus2.test-system.azgrafana-test.io/api/v5/report/kiyIZRY7k?apitoken=xxx==
```