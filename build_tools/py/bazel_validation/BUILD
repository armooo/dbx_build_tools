# @generated: This file was generated by bzl. Do not modify!
# Argument overrides and custom targets should be specified in BUILD.in.

load("//build_tools/py:py.bzl", "dbx_py_binary", "dbx_py_library", "dbx_py_pytest_test")

dbx_py_library(
    name = "bazel_deps",
    srcs = ["bazel_deps.py"],
    python2_compatible = False,
    python3_compatible = True,
    validate = "strict",
    deps = [
        ":builtins",
        "//build_tools/bzl_lib:parse_py_imports_lib",
        "//build_tools/py:python_encoding",
        "//pip/pathlib",
        "//pip/typed-ast",
        "//pip/typing",
    ],
)

dbx_py_pytest_test(
    name = "bazel_deps_test",
    srcs = ["bazel_deps_test.py"],
    python2_compatible = False,
    python3_compatible = True,
    deps = [
        ":bazel_deps",
        "//pip/pathlib",
        "//pip/typing",
    ],
)

dbx_py_binary(
    name = "check_bazel_deps",
    srcs = ["check_bazel_deps.py"],
    main = "check_bazel_deps.py",
    python = "//thirdparty/cpython:drte-interpreter-37",
    python2_compatible = False,
    python3_compatible = True,
    validate = "strict",
    visibility = ["//visibility:public"],
    deps = [
        ":bazel_deps",
        "//pip/pathlib",
        "//pip/typing",
    ],
)

dbx_py_library(
    name = "builtins",
    srcs = ["builtins.py"],
    python2_compatible = False,
    python3_compatible = True,
    validate = "strict",
    deps = [
        "//pip/typing",
    ],
)
