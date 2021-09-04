FROM rockylinux/rockylinux:8.4 

#安装kubectl
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin/kubectl

#安装kubeconfig
RUN mkdir /root/.kube
ADD /root/.kube/config /root/.kube/config

#提供默认的ssh key
RUN usermod -p "!" root
ADD /root/.ssh/id_rsa /root/.ssh/id_rsa
RUN cat /root/.ssh/id_rsa.pub >> /root/.ssh/authorized_keys
