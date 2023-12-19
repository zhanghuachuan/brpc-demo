# brpc-demo
基于bazel搭建brpc的demo：

## 环境

- bazel version:4.2.1
- jdk1.8

## 使用

编译server

```
bazel build //module1:echo_server
```

编译client

```
bazel build //module1:echo_client
```

启动server

```
sh -c ./bazel-bin/module1/echo_server
```

启动client

```
sh -c ./bazel-bin/module1/echo_client
```

