# Kubernetes Manifests for Example Application

This repository contains Kubernetes manifests for deploying an example application. The manifests include configurations for Namespace, Secret, ConfigMap, Deployment, Service, Ingress, Horizontal Pod Autoscaler (HPA), Persistent Volume (PV), Persistent Volume Claim (PVC), and Storage Class for Amazon EFS.

## Directory Structure

k8s-manifest/
├── namespace.yaml
├── secret.yaml
├── configmap.yaml
├── deployment.yaml
├── service.yaml
├── ingress.yaml
├── hpa.yaml
├── pv.yaml
├── pvc.yaml
└── storageclass.yaml


## Prerequisites

- Kubernetes cluster
- `kubectl` command-line tool configured to interact with your cluster
- Amazon EFS set up (for persistent storage)

## Applying the Manifests

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/k8s-manifest.git
    cd k8s-manifest
    ```

2. Apply the namespace:
    ```sh
    kubectl apply -f namespace.yaml
    ```

3. Apply the secret:
    ```sh
    kubectl apply -f secret.yaml
    ```

4. Apply the configmap:
    ```sh
    kubectl apply -f configmap.yaml
    ```

5. Apply the persistent volume and persistent volume claim:
    ```sh
    kubectl apply -f pv.yaml
    kubectl apply -f pvc.yaml
    ```

6. Apply the storage class (if needed):
    ```sh
    kubectl apply -f storageclass.yaml
    ```

7. Apply the deployment:
    ```sh
    kubectl apply -f deployment.yaml
    ```

8. Apply the service:
    ```sh
    kubectl apply -f service.yaml
    ```

9. Apply the ingress:
    ```sh
    kubectl apply -f ingress.yaml
    ```

10. Apply the horizontal pod autoscaler:
    ```sh
    kubectl apply -f hpa.yaml
    ```

## Explanation of Manifests

- **namespace.yaml**: Defines a namespace for the application resources.
- **secret.yaml**: Contains secrets used by the application.
- **configmap.yaml**: Contains configuration data that can be injected into pods.
- **deployment.yaml**: Defines a deployment for the application pods.
- **service.yaml**: Exposes the application pods internally within the cluster.
- **ingress.yaml**: Provides external access to the service via an ingress controller.
- **hpa.yaml**: Automatically scales the number of pods based on CPU usage.
- **pv.yaml**: Defines a persistent volume backed by Amazon EFS.
- **pvc.yaml**: Defines a persistent volume claim to use the persistent volume.
- **storageclass.yaml**: Defines a storage class for dynamic provisioning of EFS volumes.

## Notes

- Replace placeholders such as `your-secret` and `fs-12345678` with your actual values.
- Ensure that your EFS setup is correctly configured and accessible from your Kubernetes cluster.

## License

This project is licensed under the MIT License.

