load("//src/main/starlark/release:packager.bzl", "release_archive")
load("@bazel_skylib//:bzl_library.bzl", "bzl_library")

release_archive(
    name = "pkg",
    srcs = [
        "BUILD",
        "BUILD.com_github_jetbrains_kotlin.bazel",
        "compiler.bzl",
    ] + glob(["capabilities_*.bazel"]),
)

bzl_library(
    name = "kotlin",
    srcs = glob(["*.bzl"]),
    visibility = ["//:__subpackages__"],
)
