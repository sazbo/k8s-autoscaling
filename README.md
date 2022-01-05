# K8S AUTOSCALING

### With this kubernetes yaml file, you can create a deployment which has the specific features:

### RollingUpdate:
if the image has changes, an update will schedule new pods with the new version, in the following way:
- creates new a pod or pods (depends in maxSurge variable) with the new images
- removes pods with the old image
These steps will repeat until there are only replicas with the new image


### Horizontal Pod Autoscaling:
important: the pods in the deployment has to have resource claims
The HPA will manage the number of replicas automatically based on the atual resource usage of the pods within the specified range
