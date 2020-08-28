# k8s-rancher-harness-demo

## YouTube Walkthrough Link

https://youtu.be/FMxPRegLg-A

## SSH
```
ssh-keygen -t ecdsa -C username
```
```
xclip -sel clip < ~/.ssh/id_ecdsa.pub
```
```
ssh -i ~/.ssh/id_ecdsa.pub username@external-ip
```
## Docker Installation - Ubuntu 18.04
```
sudo apt update
```
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```
```
sudo apt update
```
```
apt-cache policy docker-ce
```
```
sudo apt install docker-ce
```
```
sudo systemctl status docker
```
```
sudo usermod -aG docker ${USER}
```
```
sudo su - ${USER}
```
```
id -nG
```
```
docker info
```
## Rancher Installation
```
sudo docker run -d --restart=unless-stopped -p 80:80 -p 443:443 -v ~/.rancher-data:/var/lib/rancher rancher/rancher
```
## ELK Setup

https://bitnami.com/stack/elk/cloud

## Slack setup

https://api.slack.com

## Harness Delegate Installation
```
sudo nano harness-delegate.sh
```
```
Ctrl+O
```
```
Ctrl+X
```
```
sudo chmod +x harness-delegate.sh
```
```
./harness-delegate.sh
```
## Helm Install in Harness Delegate Profile
```
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
```
```
chmod 700 get_helm.sh
```
```
./get_helm.sh
```
## Bitnami Repo in Harness Connectors

https://charts.bitnami.com/bitnami

## Chart Specs in Application's Service

Chart name: ```bitnami/parse```

Chart version: ```11.0.4```










