# Kubespray-Haproxy-Keepalived
A kubernetes installation with Haproxy and keepalived configured.\
The point of using these services  is to reduce access to api server , loadbalance api server requests and Ha api servers requests on port 6443/ 
First you should define a VIP and then configure check_apiserver.sh and keepalived.conf.\
check_apiserver.sh is a script that handle VIP should set on which keepavlied node , or set master or backend status on current node.\
on haproxy we set VIP on FRONTEND like VIP:6443 and we point FRONTEND section to backend server which they should be master nodes or any nodes that have api server .\
# helm charts

### Simple render 
Its a simple values.yml multi container that you only need to define container section and all, but if you want to use it you develop it by yourself.

### SonarQube helm chart: 
 The helm chart generate two pods :\
  1- sonarqube<br/> 
  2- postgresql
  
Helm chart contains some feature which i mention them:\
  1- NodeAffinity\
  2- Toleration\
  3- Non define pvc , pvc , services ( You dont need to add extra configuration directives to manifests )\
  4- Ingress\
  5- .env for application which has env varibales\
  6- Security Context ( UID,GID,FSGROUP,CAPABILITIES )\ 
  7- multi variables
  
**Sonarqube helm chart is not specified to any app and its a public template**.

