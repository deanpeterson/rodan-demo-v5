# Trusted Application Pipeline Software Template

This application, **rodan-demo-v5**, was created from a Trusted Application Pipeline Software Template.

The software templates create a new source and gitops deployment repositories with a sample source application. 

## Repositories

The source code for your application can be found in [https://github.com/deanpeterson/rodan-demo-v5 ](https://github.com/deanpeterson/rodan-demo-v5 ).
 
The gitops repository, which contains the kubernetes manifests for the application can be found in 
[https://github.com/deanpeterson/rodan-demo-v5-gitops ](https://github.com/deanpeterson/rodan-demo-v5-gitops ) 

## Application namespaces 

The default application will be found in the following namespaces. Applications can be deployed into unique namespaces or multiple software templates can also bet generated into the same group namespaces.  

|  Namespace   |  Description   |  
| -------- | -------- |
| **rodan-demo-ci** | The namespace used for CI workloads |
| **rodan-demo-development** | The default application during development. Every build will be deployed to this namespace for testing. |
| **rodan-demo-stage** | The staging namespace for this application. Promotion from development to stage is manual via an update to the [gitops repository](https://github.com/deanpeterson/rodan-demo-v5-gitops ) in the components/rodan-demo-v5/overlays/stage directory |
| **rodan-demo-prod** | The production namespace for this application. Promotion from stage to production is manual via an update to the [gitops repository](https://github.com/deanpeterson/rodan-demo-v5-gitops ) in the components/rodan-demo-v5/overlays/prod directory |