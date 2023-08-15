# hello_world_in_gke

<br>
creating docker image: docker build -t my-python-app .
<br>
docker tag my-python-app gcr.io/google-cloud-project/my-python-app
<br>
docker push gcr.io/google-cloud-project/my-python-app
<br>
gcloud container clusters create --num-nodes=1 --zone=us-central1-a
<br>
kubectl get nodes
<br>
kubectl logs pods_name
<br>
kubectl get pods
<br>
kubectl apply -f deployment.yaml
<br>
kubectl apply -f service.yaml
<br>
gcloud container clusters delete my-cluster --zone=us-central1-a
