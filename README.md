# conversao-temperatura


## Run Docker
1. RUN git clone git@github.com:Sysnando/conversao-temperatura.git
2. RUN docker image build -t sysfel/conversao-temperatura:v1 . --build-arg TAG="17-alpine3.14"
3. RUN docker container run -d -p 8081:8081 sysfel/conversao-temperatura:v2
4. OPEN browser http://localhost:8081


## Run Kubernetes (only on replicaset)
1. RUN git clone git@github.com:Sysnando/conversao-temperatura.git
2. GOTO ./src
3. RUN docker image build -t sysfel/conversao-temperatura:v2 . --build-arg TAG="17-alpine3.14"
4. GOTO ./k8s 
5. RUN k3d cluster create aula1 --agents 2 --servers 2 -p "8081:31000@loadbalancer"
6. RUN kubectl apply -f replicaset.yaml
7. OPEN browser http://localhost:8081