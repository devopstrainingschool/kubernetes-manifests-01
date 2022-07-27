# kubernetes-manifests-01
### Let create a file name deployment.yaml
```
touch deployment.yaml
```
vi inside the file and copy and paste the below
```
vi deployment.yaml
```
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

        app: my-app

    spec:

      containers:

      - name: my-app-01

        image: apiVersion: apps/v1

        ports:
        - containerPort: 8080
  ```
  ## let create the object using kubernetes manifest
  ```
  kubectl create -f deployment.yaml
  ```
  ## let check if the pods are running properly
  ```
  kubectl get pods -A
  ```
  ## Let see what is inside one container
  ```
  kubectl describe pod container-name-here
  ```
  
  ## make sure you destroy at the end
  ```
  kubectl delete deployment first-deployment
  ```
