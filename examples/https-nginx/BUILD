package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "https-nginx",
    importpath = "k8s.io/kubernetes/examples/https-nginx",
    library = ":go_default_library",
)

go_library(
    name = "go_default_library",
    srcs = ["make_secret.go"],
    importpath = "k8s.io/kubernetes/examples/https-nginx",
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/install:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
