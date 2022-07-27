# kubernetes-manifests-01
```
apiVersion: apps/v1

kind: Deployment

metadata:

  name: first-deployment

spec:

  selector:

    matchLabels:

      app: my-app

  replicas: 2 # tells deployment to run 2 pods matching the template

  template:

    metadata:

      labels:

        app: app

    spec:

      containers:

      - name: my-app

        image: apiVersion: apps/v1

        ports:
        - containerPort: 8080
  ```
