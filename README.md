# kubernetes-101

Selected Kubernetes 101 code samples borrowed from https://github.com/googlecodelabs/orchestrate-with-kubernetes

## Steps to install kubectl on Cloud Console

* `mkdir -p ~/bin`
* `cd ~/bin`
* `curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl`
* `chmod 755 ~/bin/kubectl`


## Pod Readiness Check

* Forward port 81 to port 10081
`kubectl port-forward healthy-monolith 10081:81`
* Run below curl to turn off readiness of the pod
`curl http://127.0.0.1:10081/readiness/status`
* Wait 45 seconds for the readiness to become fail
* Use `kubectl describe pod` to get details of readiness status
* Notice events
* Run curl again to force readiness to pass 
* Wait 15 seconds
* Run kubectl get and kubectl describe to verify the pod is ready again.

## Update image on deployment

* Use below command to update image on deployment
`kubectl set image deployment/hello hello=kelseyhightower/hello:2.0.0`
* Describe pods to view update events.
