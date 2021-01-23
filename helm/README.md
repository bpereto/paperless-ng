# Install paperless-ng on k8s

helm repo add bitnami https://charts.bitnami.com/bitnami
helm dep update

kubectl create namespace paperless

helm upgrade --install paperless-ng . -f values.yaml --namespace paperless
