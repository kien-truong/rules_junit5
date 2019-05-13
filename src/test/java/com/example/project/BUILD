package(
    default_visibility = ["//src/test:__subpackages__"],
)

load("//junit5:junit5.bzl", "java_junit5_test")

# Use java_test after bazel officially support junit5
java_junit5_test(
    name = "project",
    srcs = glob([
        "CalculatorTests.java",
    ]),
    test_package = "com.example.project",
    deps = [
        "//src/main/java/com/example/project",
        "@maven//:org_junit_jupiter_junit_jupiter_api",
        "@maven//:org_junit_jupiter_junit_jupiter_params",
    ],
)
