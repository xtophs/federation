load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "aggregator.go",
        "doc.go",
        "prefix.go",
        "reader.go",
        "report.go",
        "scale.go",
        "sinker.go",
        "tee.go",
    ],
    importpath = "github.com/vmware/govmomi/vim25/progress",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "aggregator_test.go",
        "common_test.go",
        "prefix_test.go",
        "reader_test.go",
        "scale_test.go",
        "tee_test.go",
    ],
    importpath = "github.com/vmware/govmomi/vim25/progress",
    library = ":go_default_library",
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
    visibility = ["//visibility:public"],
)
