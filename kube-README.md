#postgres deployment:

kubectl apply -f db-data-volume-persistentvolumeclaim.yaml
kubectl apply -f db-deployment.yaml
kubectl apply -f db-deployment.yaml

VAlidate DB pod:
kubectl exec -it db-c76b6cbc9-c45mk bash
psql -U postgres

#********************************
#Backend deployment

MOram pushati image backend aplikcaije koja se spaja na postgres DB gdje je hostname=postgres