# conversao-temperatura

1. run git@github.com:Sysnando/conversao-temperatura.git
2. run docker image build -t sysfel/conversao-temperatura:v1 . --build-arg TAG="17-alpine3.14"
3. docker container run -d -p 8080:8080 sysfel/conversao-temperatura:v1
4. Open the localhost:8080 on the browser
