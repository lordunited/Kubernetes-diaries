# SonarQube helm chart: 
The helm chart generate two pods :
  1- sonarqube 
  2- postgresql
Helm chart contains some feature which i mention them:
  1- NodeAffinity
  2- Toleration
  3- Non define pvc , pvc , services ( You dont need to add extra configuration directives to manifests )
  4- Ingress 
  5- .env for application which has env varibales
  6- Security Context ( UID,GID,FSGROUP,CAPABILITIES ) 
  7- multi variables 
Sonarqube helm chart is not specified to any app and its a public template.

