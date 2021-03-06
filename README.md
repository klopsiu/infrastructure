### Instruction - How to start.

##### Ubuntu packages to setup.

1.Install virtualbox as our VM provider:
```
sudo apt install virtualbox
```
2.Install vagrant
```
sudo apt-get install vagrant
```
3.Install ansible for provisioning
```
sudo apt-add-repository ppa:ansible/ansible 
sudo apt update
sudo apt install ansible
```

##### For different OS, please download latest packages from official sites.
##### Next steps are the same.

4.Setup dockerhub credentials in:
```
./provisioner/roles/master_node_conf/vars/main.yml
```
5.Run infrastructure.
```
vagrant up
```

6.Go to master node and check pods.
```shell
vagrant ssh master
kubectl get pods --namespace santander
```
7.Check if everything works in your browser on localhost:8110/8111/8112 (one of them).
