# Devopstest

1. Install and setup minikube: https://minikube.sigs.k8s.io/docs/start/ and I will be using vanilla Kubernetes for my whole test
2. Creating a profile for creating instances that can be used for both Infinispan and Keycloak
3. For setting up Infinispan I used their official blog for Minikube setup: https://infinispan.org/blog/tags/minikube/ and files from: https://github.com/infinispan-demos/infinispan-kubernetes
4. After that to the same Minikube I added Keycloak operator by using their official documentation here: https://www.keycloak.org/operator/installation
5. It looks like that the official documention was probably outdated and caused me some issue with accessing the site, so I found this discussion and tweak my files a bit: [https://github.com/keycloak/keycloak/issues/14666#issuecomment-1461028049](https://github.com/keycloak/keycloak/issues/14666#issuecomment-1461028049)
7. Opening the link https://test.keycloak.org:8443 and getting the main page of the Keycloak 
