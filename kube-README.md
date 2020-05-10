#postgres deployment:

kubectl apply -f db-data-volume-persistentvolumeclaim.yaml
kubectl apply -f db-deployment.yaml
kubectl apply -f db-service.yaml

#Backend deployment
kubectl apply -f backend-deployment.yaml
kubectl apply -f backend-service.yaml

#Frontend deployment
kubectl apply -f frontend-deployment.yaml
kubectl apply -f frontend-service.yaml

I test na:
http://localhost:30701/product

VAlidate DB pod:
kubectl exec -it db-c76b6cbc9-c45mk bash
psql -U postgres


MOram pushati image backend aplikcaije koja se spaja na postgres DB gdje je hostname=postgres