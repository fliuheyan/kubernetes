package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["ovirt.go"],
    importpath = "k8s.io/kubernetes/pkg/cloudprovider/providers/ovirt",
    deps = [
        "//pkg/cloudprovider:go_default_library",
        "//pkg/controller:go_default_library",
        "//vendor/gopkg.in/gcfg.v1:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["ovirt_test.go"],
    embed = [":go_default_library"],
    importpath = "k8s.io/kubernetes/pkg/cloudprovider/providers/ovirt",
    deps = ["//pkg/cloudprovider:go_default_library"],
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
