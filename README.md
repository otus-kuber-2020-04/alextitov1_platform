# alextitov1_platform
alextitov1 Platform repository
OUTSTANDING
    Dashboard: -  https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/
    k9s: -  https://k9scli.io/
    forwarder -  https://kube-forwarder.pixelpoint.io/

Git
    git clone https://github.com/otus-kuber-2020-04/alextitov1_platform
    git checkout -b kubernetes-prepare
    git add -A
    git commit -am 'Add hw files'
    git push origin kubernetes-prepare



Minikube (https://172.17.145.178:8443)
    Installation: https://kubernetes.io/docs/tasks/tools/install-minikube/

    start: minikube start --driver=hyperv #under elevated admin
    minikube.exe status
    minikube.exe ssh

Docker
    docker ps
    docker rm -f $(docker ps -a -q)
    docker build -t web:0.1 .
    docker run -itd -p 8000:8000 web:0.1
    docker tag web:0.1 alextitov1/web:0.1
    docker login
    docker push alextitov1/web:0.1




Kubectl
    kubectl cluster-info
    kubectl create namespace demo-1
    kubectl get namespaces
    kubectl get pods -n kube-system
    kubectl delete pod --all -n kube-system
    kubectl get componentstatuses  #kubectl get cs

     kubectl describe pod web
     kubectl get pod web -o yaml #выводит манифест и дополнительное описание



    kubectl exec -ti alextitov1/web -- sh


Init containers  https://kubernetes.io/docs/concepts/workloads/pods/init-containers/
