package(default_visibility = ["//visibility:public"])


cc_library(
    name = "bench",
    srcs = [
        "bench.cc"
    ],
    deps = [
        "//sparsehash:dense_hash_lib",
        "//sparsehash:sparse_hash_lib",
    ]

)


cc_library(
  name = "frontend",
  srcs = [
    "testmain.cc",
  ],
  copts = [
    "-Wall",
    "-O3",
    "-D_SPARSEHASH_CI_TESTING_",
    "-Wno-missing-field-initializers",
  ],
  linkopts = ["-pthread"],
  deps = [
    "//sparsehash:dense_hash_lib",
    "//sparsehash:sparse_hash_lib",       
    "//tests/gtest:gtest",
  ] 
)

cc_binary(
    name = "simple_unittests",
    srcs = [
        "simple_unittests.cc"
    ],
    deps = [
        "//tests/gtest:gtest",
        "//tests:frontend",
        "//sparsehash:sparse_hash_lib",
        "//sparsehash:dense_hash_lib",
    ],
    copts = [
    "-Wall",
    "-O3",
    "-D_SPARSEHASH_CI_TESTING_",
    "-Wno-missing-field-initializers",
  ],
    linkopts = ["-pthread"]
)