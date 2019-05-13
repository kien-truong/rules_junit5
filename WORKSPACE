load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "2.1"

RULES_JVM_EXTERNAL_SHA = "515ee5265387b88e4547b34a57393d2bcb1101314bcc5360ec7a482792556f42"

http_archive(
    name = "rules_jvm_external",
    sha256 = RULES_JVM_EXTERNAL_SHA,
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

JUNIT_VERSION = "5.4.2"

maven_install(
    artifacts = [
        "org.junit.platform:junit-platform-console-standalone:jar:1.4.2",
        "org.junit.jupiter:junit-jupiter:jar:%s" % JUNIT_VERSION,
    ],
    repositories = [
        "https://repo1.maven.org/maven2",
    ],
)
