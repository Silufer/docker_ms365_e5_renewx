# Intro
This docker is based on **SundayRX's E5 Renew X**

## Links

[SundayRX](https://blog.csdn.net/qq_33212020/article/details/119747634)

[E5 Renew X](https://blog.csdn.net/qq_33212020/article/details/119747634)

[Docker Hub](https://hub.docker.com/r/xntu/ms365_e5_renewx)

## Deploy

Pull image
`docker pull xntu/ms365_e5_renewx:latest`  

### Deploy with Docker CLI

```
docker run -d \
    -p 1066:1066 \
    --name RenewX \
gladtbam/ms365_e5_renewx:latest
```

> PS: The default password is: abcd1234

### Custom configuration

1. Download Config.xml，and follow the instructions

2. Run  
```
docker run -d \
    -p 1066:1066 \
    -v $PWD/Deploy:/renewx/Deploy \
    -v $PWD/appdata:/renewx/appdata \
    --name RenewX \
gladtbam/ms365_e5_renewx:latest
```

>PS: Put the Config.xml file into the Deploy folder


### DockerCompose **Recommended**

```
1. Download docker-compose.yml   
`wget https://raw.githubusercontent.com/Silufer/ms365_e5_renewx/main/docker-compose.yml`

2.Run
docker-compose up -d
```
