load("@aspect_bazel_lib//lib:transitions.bzl", "platform_transition_binary")
load("@rules_cc//cc:defs.bzl", "cc_binary")

cc_binary(
    name = "hello_world_host",
    srcs = [
        "hello_world.cc",
    ],
    tags = ["platform_missing"],

)

platform_transition_binary(
    name = "hello_world_x86_64-unknown-linux-gnu",
    binary = ":hello_world_host",
    target_platform = "//bazel/platforms:x86_64-unknown-linux-gnu",
)
