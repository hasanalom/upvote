package(default_visibility = ["//upvote"])

load(
    "//upvote:builddefs.bzl",
    "py_appengine_library",
    "upvote_appengine_test",
)

# AppEngine Libraries
# ==============================================================================

py_appengine_library(
    name = "all",
    deps = [
        "//upvote/gae/datastore/models:all",
    ],
)

py_appengine_library(
    name = "test_utils",
    srcs = ["test_utils.py"],
    deps = [
        "//external:mock",
        "//upvote/gae/datastore/models:base",
        "//upvote/gae/datastore/models:bit9",
        "//upvote/gae/datastore/models:santa",
        "//upvote/gae/shared/common:settings",
        "//upvote/gae/shared/common:user_map",
        "//upvote/shared:constants",
    ],
)

py_appengine_library(
    name = "utils",
    srcs = ["utils.py"],
)

# AppEngine Unit Tests
# ==============================================================================

upvote_appengine_test(
    name = "utils_test",
    size = "small",
    srcs = ["utils_test.py"],
    deps = [
        ":utils",
        "//external:mock",
        "//upvote/gae/shared/common:basetest",
        "@absl_git//absl/testing:absltest",
    ],
)
