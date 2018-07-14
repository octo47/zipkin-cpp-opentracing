cc_library(
    name = "rapidjson",
    hdrs = glob(["3rd_party/include/zipkin/rapidjson/**/*.h"]),
    strip_include_prefix = "3rd_party/include",
)

cc_library(
    name = "zipkin",
    srcs = glob(["zipkin/src/*.cc", "zipkin/src/*.h"]),
    hdrs = glob(["zipkin/include/zipkin/*.h"]),
    strip_include_prefix = "zipkin/include",
    visibility = ["//visibility:public"],
    deps = [
        ":rapidjson",
        "@se_haxx_curl_libcurl//:curl",
    ]
)

cc_library(
    name = "zipkin_opentracing",
    srcs = glob(["zipkin_opentracing/src/*.cc", "zipkin_opentracing/src/*.h"]),
    hdrs = glob(["zipkin_opentracing/include/zipkin/*.h"]),
    strip_include_prefix = "zipkin_opentracing/include",
    visibility = ["//visibility:public"],
    deps = [
        ":zipkin",
        "@io_opentracing_cpp//:opentracing"
    ]
)

cc_library(
    name = "zipkin_example_lib",
    srcs = glob(["zipkin_opentracing/example/*.cc"]),
    hdrs = glob(["zipkin_opentracing/example/*.h"]),
    strip_include_prefix = "zipkin_opentracing/example",
    deps = [
        ":zipkin_opentracing"
    ]
)

cc_binary(
    name = "zipkin_example",
    deps = [
        ":zipkin_example_lib"
    ]
)