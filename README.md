1. # Launched ec2 (ubuntu 20.04, t2.micro) ad attached IAM role (Admin access) to it.
2. # Next cloned the github repo and run needed scripts to install terraform, eksctl, kubectl, doker and aws cli
3. git clone https://github.com/Narian318/k8s-mario.git
4. cd k8s-mario
5. vi script.sh ---> chmod +x script.sh ---> ./script.sh
6. cd EKS-TF --> terraform init --> terraform validate --> terraform plan --> terraform apply (or) terraform apply --auto-approve
7. aws eks update-kubeconfig --name EKS_CLOUD --region ap-south-1
8. cd .. ---> kubectl apply -f deployment.yaml --> kubectl apply -f service.yaml --> kubectl get svc (or) kubectl describe service mario-service (or) kubectl get all
9. # access the desired application through Load Balancer DNS link in browser
10. kubectl delete -f service.yaml --> kubectl delete -f deployment.yaml
11. cd EKS-TF --> terraform destroy --auto-approve
