# *******************************************************************************
# Copyright (c) 2025 Contributors to the Eclipse Foundation
#
# See the NOTICE file(s) distributed with this work for additional
# information regarding copyright ownership.
#
# This program and the accompanying materials are made available under the
# terms of the Apache License Version 2.0 which is available at
# https://www.apache.org/licenses/LICENSE-2.0
#
# SPDX-License-Identifier: Apache-2.0
# *******************************************************************************
load("@score_cr_checker//:cr_checker.bzl", "copyright_checker")
load("@dash_license_checker//:dash.bzl", "dash_license_checker")
load("//:project_config.bzl", "PROJECT_CONFIG")

copyright_checker(
    name = "copyright",
    srcs = [
        "src",
        "tests",
        "//:BUILD",
        "//:MODULE.bazel",
    ],
    template = "@score_cr_checker//resources:templates",
    config = "@score_cr_checker//resources:config",
    visibility = ["//visibility:public"],
)


dash_license_checker(
    visibility = ["//visibility:public"],
    src = "//examples:cargo_lock",
    file_type = "",               # let it auto-detect based on project_config
    project_config = PROJECT_CONFIG
)
