# DevOpsTest

1. Install and setup minikube: https://minikube.sigs.k8s.io/docs/start/ and I will be using vanilla Kubernetes for my whole test
2. Creating a profile for creating instances that can be used for both Infinispan and Keycloak
3. For setting up Infinispan I used their official blog for Minikube setup: https://infinispan.org/blog/tags/minikube/ and files from: https://github.com/infinispan-demos/infinispan-kubernetes and for the operator: https://infinispan.org/docs/infinispan-operator/main/operator.html#installation
4. After that to the same Minikube I added Keycloak operator by using their official documentation here: https://www.keycloak.org/operator/installation and using the "Installing by using kubectl without Operator Lifecycle Manager"
5. After that moved to: https://www.keycloak.org/operator/basic-deployment where I setup my database(I used PostgreSQL like in the documentation), hostname and certificates
6. It looks like that the official documention was probably outdated and caused me some issue with accessing the site, so I found this discussion and tweak my files a bit: [https://github.com/keycloak/keycloak/issues/14666#issuecomment-1461028049](https://github.com/keycloak/keycloak/issues/14666#issuecomment-1461028049)
7. Running the tunnel and opening the link https://test.keycloak.org:8443 and getting the main page of the Keycloak
8. Tried setting up the caching while using the official documention: https://www.keycloak.org/high-availability/connect-keycloak-to-external-infinispan and also since it is still a feature that is in preview I also was checking out the discussion and tracking it how it work for other people too(especially since it cover more IRL situations rather than just basic dev testing): https://github.com/keycloak/keycloak/discussions/25269
also checked out both: https://www.keycloak.org/high-availability/deploy-keycloak-kubernetes and https://www.keycloak.org/high-availability/deploy-infinispan-kubernetes-crossdc

Some additional and useful documention that I used that helped me understand things more: 
- https://www.keycloak.org/getting-started/getting-started-kube
- https://www.keycloak.org/server/db
- https://www.keycloak.org/server/keycloak-truststore
- https://kubernetes.io/docs/tutorials/hello-minikube/
- https://infinispan.org/docs/stable/titles/xsite/xsite.html
- https://dev.to/cockroachlabs/simulating-a-multi-region-cockroachdb-cluster-on-kubernetes-with-minikube-4jd9 (it is a different DB used here, but wanted to see how to create regions with MiniKube)
- https://infinispan.org/docs/stable/titles/xsite/xsite.html
- https://infinispan.org/docs/infinispan-operator/main/operator.html#securing-cross-site-connections_cross-site
- https://infinispan.org/docs/infinispan-operator/main/operator.html#creating-caches


My best friends in this whole test were official KeyCloak and Infinispan documentions, but you still have to check if they are not outdated, if yes, forums and GitHub discussions are your next best friends.
Also we can not forget that having good music while working is a must, here are the ones that made me feel like a main character while learning new things and working on this:
- https://www.youtube.com/watch?v=tGeYmC9bK68
- https://www.youtube.com/watch?v=QFvt2cNSOaM
- https://www.youtube.com/watch?v=6NQUbFiUYRw
- https://www.youtube.com/watch?v=McnMsFwZlvA
- https://www.youtube.com/watch?v=6U6MZC-iRyo
