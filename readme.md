### What’s included

[**Ollama**](https://ollama.com/) - Cross-platform LLM platform to install
and run the latest local LLMs

[**Open-webui**](https://qdrant.tech/) - Open-source, high performance vector
store with an comprehensive API

[**openedAI**](https://www.postgresql.org/) -  Workhorse of the Data
Engineering world, handles large amounts of data safely.

[**nginx**](https://www.postgresql.org/) -  Workhorse of the Data
Engineering world, handles large amounts of data safely.



## Installation on Linux

## 

1. Install Docker on Ubuntu https://docs.docker.com/engine/install/ubuntu/
```
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```


2. Install Nvidia Drivers
```
sudo apt update
sudo ubuntu-drivers autoinstall
sudo reboot
```

3. Install Nvidia Container Toolkit
```
curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey \
    | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg
curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list \
    | sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' \
    | sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
sudo apt-get update

sudo apt-get install -y nvidia-container-toolkit

sudo nvidia-ctk runtime configure --runtime=docker
sudo systemctl restart docker

```

4. Install LocalAI
```
git clone https://github.com/DominikHeindl/LocalAI.git
cd localAI

```



5. Run
```
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ssl/nginx.key -out ssl/nginx.crt
docker compose up
```