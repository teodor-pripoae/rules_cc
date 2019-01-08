# C++ rules for Bazel

This repository contains Starlark implementation of C++ rules in Bazel.

The rules are being incrementally converted from their native implementations in the [Bazel source tree](https://source.bazel.build/bazel/+/master:src/main/java/com/google/devtools/build/lib/rules/cpp/).

For the list of C++ rules, see the Bazel
[documentation](https://docs.bazel.build/versions/master/be/overview.html).

# Getting Started

There is no need to use rules from this repository just yet. If you want to use
rules\_cc anyway, add the following to your WORKSPACE file:

```
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
    name = "rules_cc",
    urls = ["https://github.com/bazelbuild/rules_cc/archive/TODO"],
    sha256 = "TODO",
)
```

Then, in your BUILD files, import and use the rules:

```
load("@rules_cc//cc:rules.bzl", "cc_library")
cc_library(
    ...
)
```

# Migration Tools

This repository also contains migration tools that can be used to migrate your
project for Bazel incompatible changes.