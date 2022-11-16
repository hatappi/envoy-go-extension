load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_contrib_extension",
    "envoy_contrib_package",
)

licenses(["notice"])  # Apache 2

envoy_contrib_package()

# DSO

envoy_cc_contrib_extension(
    name = "config",
    srcs = ["config.cc"],
    hdrs = [
        "config.h",
    ],
    repository = "@envoy",
    visibility = ["//visibility:public"],
    deps = [
        "//api/contrib/envoy/extensions/dso/v3:pkg_cc_proto",
        "//contrib/golang/common/dso:dso_lib",
        "@envoy//envoy/registry",
        "@envoy//envoy/server:bootstrap_extension_config_interface",
        "@envoy//envoy/server:factory_context_interface",
        "@envoy//envoy/server:instance_interface",
        "@envoy//source/common/common:assert_lib",
        "@envoy//source/common/common:empty_string",
        "@envoy//source/common/config:datasource_lib",
        "@envoy//source/common/protobuf:utility_lib",
    ],
)
