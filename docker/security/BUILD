# Copyright 2017 The Bazel Authors. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@bazel_skylib//:bzl_library.bzl", "bzl_library")
load("@pip_deps//:requirements.bzl", "requirement")
load("@subpar//:subpar.bzl", "par_binary")

package(default_visibility = ["//visibility:public"])

exports_files([
    "security_check_whitelist.json",
])

par_binary(
    name = "security_check",
    srcs = ["security_check.py"],
    main = "security_check.py",
    python_version = "PY2",
    visibility = ["//visibility:public"],
    deps = [
        requirement("PyYaml"),
    ],
)

bzl_library(
    name = "security_check_lib",
    srcs = [
        "security_check.bzl",
    ],
)
