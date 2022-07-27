# kubernetes-manifests-01
```
apiVersion: apps/v1 #  for k8s versions before 1.9.0 use apps/v1beta2  and before 1.8.0 use extensions/v1beta1
kind: Deployment
metadata:
  name: my-first-app
  labels:
    app: my-app
spec:
  containers:
  - name: php-redis
    image: gcr.io/google-samples/gb-frontend:v4
    ports:
    - containerPort: 8080
```
