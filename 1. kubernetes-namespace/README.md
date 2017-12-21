# kubernetes-namespace


#### Set default namespace
> kubectl config set-context $(kubectl config current-context) --namespace=<name>


#### Validate namespace
> kubectl config view | grep namespace:
