apiversion: apps/v1
kind: Deployment
metadata:
  name: blue-file
spec: 
  replicas:
  selector:
    matchLabels:
      app: blue
  template:
    metadata:
      labels:
        app: blue
    spec:
      containers:
      - name: c1
        image: jadhavkaveri/sanchita-repo:fairy_img
        ports:
          containerPort: 80
