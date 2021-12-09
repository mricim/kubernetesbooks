# kubernetesbooks

![image](https://user-images.githubusercontent.com/56126432/145402121-273d619c-f4da-4809-be98-1d36f1075459.png)
```
graph LR
P[Java] --> A[Jar]
P --> X((Github)) --> P
A -- build--> B[Docker]
B -- push -->C((Docker Hub))
C -- create pod --> D[kubernetes] 
```

![image](https://user-images.githubusercontent.com/56126432/145401274-1313a094-6e8b-40b2-970e-8aaed3d42fb0.png)
```mermaid
graph LR
A[LoadBalancer] --  books.ericcm.tk --> B[Traefic]
A -- booksa.ericcm.tk --> B
B --> C{Domain}
C -- books--> D[LoadBalancer]
C -- booksa --> X[LoadBalancer]
C -- books/tls --> K[NodePort]
C -- books/notls --> K[NodePort]
D --> E[Pod Client]
X --> M[Pod Server]
K --> N[Pod Whoami]
G((ReplicationController)) --> E
F((ReplicationController)) --> M
```
