# OpenCensus C++ Context library.
# See context.h for details.
#
# Copyright 2018, OpenCensus Authors
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("//opencensus:copts.bzl", "DEFAULT_COPTS", "TEST_COPTS")

licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:private"])

cc_library(
    name = "context",
    srcs = [
        "internal/context.cc",
        "internal/with_context.cc",
    ],
    hdrs = [
        "context.h",
        "with_context.h",
    ],
    copts = DEFAULT_COPTS,
    visibility = ["//visibility:public"],
    deps = [
        "//opencensus/tags",
        "//opencensus/trace",
    ],
)

# Tests
# ========================================================================= #

cc_test(
    name = "context_test",
    srcs = ["internal/context_test.cc"],
    copts = TEST_COPTS,
    deps = [
        ":context",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_test(
    name = "with_context_test",
    srcs = ["internal/with_context_test.cc"],
    copts = TEST_COPTS,
    deps = [
        ":context",
        "@com_google_googletest//:gtest_main",
    ],
)