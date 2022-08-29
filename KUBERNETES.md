# Installation instructions for Kubernetes

## Service Operator

This deployment uses service operator. It was tested with AKS using this installation guide: https://techcommunity.microsoft.com/t5/apps-on-azure-blog/using-azure-kubernetes-service-with-grafana-and-prometheus/ba-p/3020459

## 

Push the example image to your private registry.
- First build it with ```./gradlew dockerBuild ```
- Tag the image to  your private registry and push it
- Change the deployment file in /deployment to include your private registry in the container name (row 19 of deployment.yml)
- cd to deployment and apply ```kubectl apply -f deployment.yml`
- Import JVM micrometer dashboard to Grafana (import from main-menu, use id from Grafana.com)