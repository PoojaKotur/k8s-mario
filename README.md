Launched ec2 (ubuntu 20.04, t2.micro) ad attached IAM role (Admin access) to it.
Next cloned the github repo and run needed scripts to install terraform, eksctl, kubectl, doker and aws cli
git clone https://github.com/Narian318/k8s-mario.git
cd k8s-mario
vi script.sh ---> chmod +x script.sh ---> ./script.sh
cd EKS-TF --> terraform init --> terraform validate --> terraform plan --> terraform apply (or) terraform apply --auto-approve
aws eks update-kubeconfig --name EKS_CLOUD --region ap-south-1
cd .. ---> kubectl apply -f deployment.yaml --> kubectl apply -f service.yaml --> kubectl get svc (or) kubectl describe service mario-service (or) kubectl get all
access the desired application through Load Balancer DNS link in browser
kubectl delete -f service.yaml --> kubectl delete -f deployment.yaml
cd EKS-TF --> terraform destroy --auto-approve
