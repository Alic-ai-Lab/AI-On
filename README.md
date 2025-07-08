# AI-On: Web Service Portal on kubernetes for AI

AI-On is a Kubernetes-based web service portal jointly developed by KISTI and Zenitos, aimed at providing services necessary for AI development, training, and deployment.

* Currently Available Service

  1. Web-based terminal: TTYD
  2. Web-based integrated development environment: Jupyter, Visual Studio Code, RStudio
  3. Remote Desktop: VNC

* Upcoming service

  1. Distributed Training: kubeflow train operator
  2. Web-based fine tuning: Axolotl
  3. Model serving: kserve


# Requirments

* docker engine (including docker compose)
* kubernetes

# Get Started

* basic mode

```python
git clone https://github.com/Alic-ai-Lab/AI-On.git  
cd AI-On  
docker compose -f docker-compose-light.yaml up  
```
Open http://localhost:8080 in your browser

* with external authentication (keycloak + oauth2-proxy)

```python
git clone https://github.com/Alic-ai-Lab/AI-On.git  
cd AI-On  
docker compose -f docker-compose-keycloak.yaml up
```
Open http://oauth2-proxy.localtest.me:4180 in your browser

* administrator: admin/password
* user: user/password

By utilizing Keycloak and oauth2-proxy, it is possible to provide services with authentication. Configuration details for oauth2-proxy can be found at: https://github.com/oauth2-proxy/oauth2-proxy/tree/master/contrib/local-environment.

