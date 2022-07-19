# carla_apollo_bridge学习笔记

> https://github.com/AuroAi/carla_apollo_bridge

## 1. 基本原理

三个 docker container

（1）carla server 跑 Carla simulation；

（2）carla-apollo  本质上实现了message 格式的转换；

（3）跑 apollo_dev_user ；



## 2. 使用步骤

https://github.com/AuroAi/carla_apollo_bridge 有详细说明

（1）经过修改的 apollo   ： apollo发送 carla识别的消息   build， **打开并编译Apollo 端**

（2） carla docker image  carlasim/carla:0.9.6      **打开Carla server 端**

（3）Carla-Apollo bridge 打开本地功能包 container   **镜像名字carla-apollo **

```
### Build docker image / run container for Carla-Apollo bridge
This container will run the bridge and sim clients.

报错
Successfully built d37560990982
Successfully tagged carla-apollo:latest
access control disabled, clients can connect from any host
a24086ac56a472b2d1646b0c06779f2dcd77768b49f25f8cae1127f06b2e45a1

进入 carla-apollo 容器
docker exec -ti carla-apollo bash
```







## issues

（1）apollo routing 后车辆前行，但是在carla里并没有跟随这运动；

（2）如何将 carla地图转成apollo的HDmap；