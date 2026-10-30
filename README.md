# GIT

mkdir StudentProfileSystem  
cd StudentProfileSystem  
notepad student.py  
git init  
git status  
git add student.py  
git commit -m "Initial student profile system"  
git log --oneline  
git branch -M main  
git remote add origin https://github.com/YOUR_USERNAME/StudentProfileSystem.git  
git remote -v  
git push -u origin main  
git status  
git diff  
git add student.py  
git commit -m "Update student profile system"  
git push origin main  
git checkout -b feature-update  
git branch  
git add student.py  
git commit -m "Add feature update"  
git push -u origin feature-update  
git checkout main  
git pull origin main  
git log --oneline --graph --all  
git clone https://github.com/YOUR_USERNAME/StudentProfileSystem.git  
cd StudentProfileSystem  
git status  

# Docker

## EXPERIMENT 4

docker --version  
docker info  
docker pull nginx  
docker images  
docker run -d --name nginx-demo -p 8080:80 nginx  
docker ps  

### Open http://localhost:8080

docker stop nginx-demo  
docker rm nginx-demo  
docker rmi nginx  

## EXPERIMENT 5

mkdir DockerDemo  
cd DockerDemo  
docker build -t flaskdemo .  
docker images  
docker run -d -p 5000:5000 flaskdemo  
docker ps  

### Open http://localhost:5000

docker logs &lt;container_id&gt;  
docker stop &lt;container_id&gt;  
docker start &lt;container_id&gt;  
docker ps  
docker stop &lt;container_id&gt;  
docker rm &lt;container_id&gt;  
docker rmi flaskdemo  

git add student.py  
git commit -m "Update forked project"  
git push origin main  

# Kubernetes

## VERIFY

minikube version  
kubectl version --client  

## CLUSTER

minikube start  
kubectl get nodes  

## DEPLOY

kubectl create deployment flaskdemo --image=YOUR_DOCKERHUB_USERNAME/flaskdemo:latest  
kubectl get deployments  
kubectl get pods  

## SERVICE

kubectl expose deployment flaskdemo --type=NodePort --port=5000  
kubectl get services  
minikube service flaskdemo  

## SCALE

kubectl scale deployment flaskdemo --replicas=3  
kubectl get pods  

## INSPECT

kubectl get all  
kubectl describe deployment flaskdemo  
kubectl logs &lt;pod-name&gt;  

## CLEANUP

kubectl delete service flaskdemo  
kubectl delete deployment flaskdemo  
minikube stop  

## OPTIONAL

minikube delete
