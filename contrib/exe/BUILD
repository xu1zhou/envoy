load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_binary",
    "envoy_contrib_package",
)
load(
    "//contrib:all_contrib_extensions.bzl",
    "envoy_all_contrib_extensions",
)

licenses(["notice"])  # Apache 2

envoy_contrib_package()

alias(
    name = "envoy-contrib",
    actual = ":envoy-contrib-static",
)

envoy_cc_binary(
    name = "envoy-contrib-static",
    stamped = True,
    deps = ["//source/exe:envoy_main_entry_lib"] + envoy_all_contrib_extensions(),
)
