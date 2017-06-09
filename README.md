# kubernetes-101

Selected Kubernetes 101 code samples borrowed from https://github.com/googlecodelabs/orchestrate-with-kubernetes

## Steps to install kubectl on Cloud Console

* `mkdir -p ~/bin`
* `cd ~/bin`
* `curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl`
* `chmod 755 ~/bin/kubectl`
