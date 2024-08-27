apiVersion: apps/v1 

kind: Deployment 

metadata: 

  name: counterapp 

  labels: 

    product: counterapp 

spec: 

  replicas: 1 

  selector: 

    matchLabels: 

      app: counterapp 

  template: 

    metadata: 

      labels: 

        app: counterapp 

    spec: 

      containers: 

      - name: bootcamp-container 

        image: jocatalin/kubernetes-bootcamp:v1 

        ports: 

 

        - containerPort: 8080 

        resources: 

          limits: 

            cpu: "1" 

            memory: "600Mi" 

          requests: 

            cpu: "500m" 

            memory: "300Mi" 
