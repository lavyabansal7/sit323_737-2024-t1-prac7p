### Setting Up Kubernetes Cluster and Deploying a Containerized Node.js Application

#### Steps

**1. Enable Kubernetes in Docker Application**
   - Next, we Verify Kubernetes Cluster Info using these commands:
     ```bash
     kubectl cluster-info
     kubectl get nodes
     ```

**2. Build and Push Docker Image**
   - Build Docker Image:
     ```bash
     docker build -t yourusername/yourimage:latest .
     ```
   - Tag and Push Image:
     ```bash
     docker push yourusername/yourimage:latest
     ```

**3. Create Kubernetes Deployment and Service**
   - Create Pods:
     ```bash
     kubectl apply -f createPods.yaml
     ```

   - Create Deployment:
     ```bash
     kubectl apply -f createDeployment.yaml
     ```
   - Create Service:
     ```bash
     kubectl apply -f createService.yaml
     ```

**4. Verify Service**
   - After applying the Service configuration, use the following command to verify the status of the service, including its ClusterIP or NodePort:
     ```bash
     kubectl get svc
     ```
