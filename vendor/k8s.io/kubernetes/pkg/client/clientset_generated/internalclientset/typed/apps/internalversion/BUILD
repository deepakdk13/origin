package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "apps_client.go",
        "controllerrevision.go",
        "doc.go",
        "generated_expansion.go",
        "statefulset.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/client/clientset_generated/internalclientset/typed/apps/internalversion",
    deps = [
        "//pkg/apis/apps:go_default_library",
        "//pkg/apis/autoscaling:go_default_library",
        "//pkg/client/clientset_generated/internalclientset/scheme:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//staging/src/k8s.io/client-go/rest:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//pkg/client/clientset_generated/internalclientset/typed/apps/internalversion/fake:all-srcs",
    ],
    tags = ["automanaged"],
)
