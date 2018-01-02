# kubernetes-namespace


#### Create mongo pod and services
> kubectl create -f mongo-rc.yml<br>
> kubectl create -f mongo-svc.yml

#### Create user pod
> kubectl create -f user-pod.yml


#### Troubleshooting commands
> kubectl describe pod user --namespace=demo<br>

> kubectl get pod user --namespace=demo<br>
> kubectl get pod user --namespace=demo -o=json<br>
> kubectl get pod user --namespace=demo -o=yaml<br>
> kubectl get pod user --namespace=demo -o=wide<br>

#### Access pod application from local machine
> kubectl port-forward user 8012:8012 --namespace=demo<br>

#### Access pod shell
> kubectl exec -it user -- /bin/bash

#### Access minikube node
> ssh -i ~/.minikube/machines/minikube/id_rsa docker@$(minikube ip)

#### Access pod logs
> kubectl logs user --namespace=demo

#### Copying files to and from Containers
> kubectl cp <pod-name>:/captures/capture3.txt ./capture3.txt<br>
> kubectl cp $HOME/config.txt <pod-name>:/config.txt

#### Show labels
> kubectl get pod user --show-labels --namespace=demo

#### Set default namespace
> kubectl config set-context $(kubectl config current-context) --namespace={name}

#### Validate namespace
> kubectl config view | grep namespace:
