# hello_world_in_gke


Google Cloud Platform (GCP) provides a set of command-line tools for managing Kubernetes clusters on its platform. These tools are part of the `gcloud` command-line interface. Here's a list of some common `gcloud` commands for working with Google Kubernetes Engine (GKE), along with explanations:

1. **Cluster Management:**
   - `gcloud container clusters create [CLUSTER_NAME]`: Creates a new GKE cluster with the specified name.
   - `gcloud container clusters get-credentials [CLUSTER_NAME]`: Retrieves cluster credentials and configures `kubectl` to interact with the specified cluster.
   - `gcloud container clusters delete [CLUSTER_NAME]`: Deletes the specified GKE cluster.
   - `gcloud container clusters list`: Lists all GKE clusters in the current project.

2. **Node Pools:**
   - `gcloud container node-pools create [POOL_NAME] --cluster [CLUSTER_NAME]`: Creates a new node pool within a GKE cluster.
   - `gcloud container node-pools delete [POOL_NAME] --cluster [CLUSTER_NAME]`: Deletes a specific node pool from a GKE cluster.

3. **Cluster Upgrades:**
   - `gcloud container clusters upgrade [CLUSTER_NAME]`: Initiates a cluster upgrade to the latest available version of Kubernetes.

4. **Node Management:**
   - `gcloud container node-pools resize [POOL_NAME] --num-nodes [NEW_NODE_COUNT] --cluster [CLUSTER_NAME]`: Resizes the node pool to the specified number of nodes.
   - `gcloud container node-pools update [POOL_NAME] --cluster [CLUSTER_NAME] --node-taints [TAINTS]`: Updates the node pool configuration, including taints.

5. **Workload Management:**
   - `kubectl apply -f [CONFIG_FILE]`: Applies a Kubernetes configuration file to create or update resources.
   - `kubectl get pods`: Lists all pods running in the currently configured cluster.
   - `kubectl describe pod [POD_NAME]`: Provides detailed information about a specific pod.

6. **Horizontal Pod Autoscaling:**
   - `kubectl autoscale deployment [DEPLOYMENT_NAME] --min [MIN_REPLICAS] --max [MAX_REPLICAS] --cpu-percent [TARGET_CPU_PERCENT]`: Sets up horizontal pod autoscaling for a deployment.

7. **Network Policies:**
   - `kubectl create -f [POLICY_FILE]`: Creates a network policy to control traffic flow between pods.
   - `kubectl get networkpolicies`: Lists all network policies in the current namespace.

8. **Ingress and Services:**
   - `kubectl expose deployment [DEPLOYMENT_NAME] --port [PORT] --target-port [TARGET_PORT] --type [SERVICE_TYPE]`: Exposes a deployment as a service.
   - `kubectl create -f [INGRESS_FILE]`: Creates an ingress resource to manage external access to services.

9. **Logging and Monitoring:**
   - `gcloud logging read "resource.type=k8s_container AND resource.labels.cluster_name=[CLUSTER_NAME]"`: Reads logs from Kubernetes containers in a specific cluster.
   - `gcloud monitoring dashboards create --config-from-file=[DASHBOARD_CONFIG_FILE]`: Creates a monitoring dashboard from a JSON/YAML configuration file.

These commands provide a foundation for managing Google Kubernetes Engine clusters and workloads. Keep in mind that command options, syntax, and behaviors can change, so it's important to refer to the official documentation for the most up-to-date information when working with GKE.
