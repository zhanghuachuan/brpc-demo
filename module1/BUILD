

proto_library(
    name = "echo_proto",
    srcs = [
        "proto/echo.proto",
    ],
)
# 将pb编译声明为一个依赖dep
cc_proto_library(
    name = "cc_echo_proto",
    deps = [
        ":echo_proto",
    ],
)

# 二进制文件的依赖依赖于上面声明的dep
cc_binary(
    name = "echo_server",
    srcs = [
        "server.cpp",
    ],
    deps = [
        ":cc_echo_proto",
        "@brpc//:brpc",
    ],
)

cc_binary(
    name = "echo_client",
    srcs = [
        "client.cpp"
    ],
    deps = [
        ":cc_echo_proto",
        "@brpc//:brpc",
    ],
    
)
