- Use the kind-deployment.yaml to creat ethe kind eks cluster with 3 nodes.
# use the below command to creat ethe cluster
#1.
cat > ~/k8s-practice/kind-cluster.yaml <<'EOF'
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
- role: control-plane
- role: worker
- role: worker
- role: worker 
EOF

2. 
kind create cluster --name practice --config ~/k8s-practice/kind-cluster.yaml  #command to create the cluster using above yaml
kubectl get nodes
