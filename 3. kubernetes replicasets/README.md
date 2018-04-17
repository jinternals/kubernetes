# kubernetes-replicasets


#### create replica sets
> kubectl create -f demo-rs.yml<br>


#### delete replica sets
> kubectl delete rs hello-rs --namespace=demo <br>
> kubectl delete rs hello-rs --namespace=demo --cascade=false <br>



>kubectl get pods --namespace=demo --show-labels <br>