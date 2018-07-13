workspace(name = "com_github_rnburn_zipkin_opentracing")

git_repository(
    name = "io_opentracing_cpp",
    remote = "https://github.com/opentracing/opentracing-cpp",
    commit = "ac50154a7713877f877981c33c3375003b6ebfe1",
)

new_http_archive(
    name = "se_haxx_curl_libcurl",
    sha256 = "ff3e80c1ca6a068428726cd7dd19037a47cc538ce58ef61c59587191039b2ca6",
    urls = [
        "http://bazel-mirror.storage.googleapis.com/curl.haxx.se/download/curl-7.49.1.tar.gz",
        "https://curl.haxx.se/download/curl-7.49.1.tar.gz",
    ],
    strip_prefix = "curl-7.49.1",
    build_file = "3rd_party/curl.BUILD"
)

new_http_archive(
      name = "zlib_archive",
      urls = [
          "https://mirror.bazel.build/zlib.net/zlib-1.2.11.tar.gz",
          "https://zlib.net/zlib-1.2.11.tar.gz",
      ],
      sha256 = "c3e5e9fdd5004dcb542feda5ee4f0ff0744628baf8ed2dd5d66f8ca1197cb1a1",
      strip_prefix = "zlib-1.2.11",
      build_file = "3rd_party/zlib.BUILD"
  )