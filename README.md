Local K8s deployment with Kind using Kustomize
- Since it is using Kind, have to specify NodePort to be able to call service
- Split up into `base`, `testing`, `staging`
--> testing adds a specific namespace, testing- prefix, configMap with a testing.env file
--> staging adds a specific namespace, staging- prefix, configMap with a staging.env file, new image
