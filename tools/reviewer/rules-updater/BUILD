load("//tools/checkstyle:checkstyle.bzl", "checkstyle_test")

java_binary(
    name = "rules_updater",
    srcs = ["RulesUpdater.java"],
    main_class = "com.google.startupos.tools.reviewer.rules_updater.RulesUpdater",
    deps = [
        "//common",
        "//common:dagger_with_annotation_processor",
        "//common/flags",
        "//third_party/maven/com/google/flogger:flogger_system_backend",
        "//tools/reviewer:reviewer_java_proto",
    ],
)

checkstyle_test(
    name = "rules_updater-checkstyle",
    allow_failure = 1,
    target = ":rules_updater",
)
