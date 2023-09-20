# GSP736
>🚨 [PLEASE SUBSCRIBE OUR CHANNEL CLOUDHUSTLER](https://www.youtube.com/@cloudhustlers) **&** [JOIN OUR COMMUNITY](https://chat.whatsapp.com/KBfUcSleGGEFf2Xvvm8FW3)
### Run in cloudshell
```cmd
export ZONE=
```
```cmd
gcloud container clusters get-credentials central --zone $ZONE
git clone https://github.com/xiangshen-dk/microservices-demo.git
cd microservices-demo
kubectl apply -f release/kubernetes-manifests.yaml
export EXTERNAL_IP=$(kubectl get service frontend-external | awk 'BEGIN { cnt=0; } { cnt+=1; if (cnt > 1) print $4; }')
curl -o /dev/null -s -w "%{http_code}\n"  http://$EXTERNAL_IP
```
> Search ```logging``` > create matrix

> Name ```Error_Rate_SLI``` > Paste the below code in build filter > Create Metric
```cmd
resource.type="k8s_container"
severity=ERROR
labels."k8s-pod/app": "recommendationservice"
```
> Perform task 5 manually 
