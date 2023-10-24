package(default_visibility = ["//visibility:public"])


cc_library(
    name = "dense_hash_lib",
    srcs = [
        "dense_hash_map.h",
        "dense_hash_set.h",
    ],
    deps = [
        "//sparsehash/internal:hash_table_lib"
    ]
)

cc_library(
    name = "sparse_hash_lib",
    srcs = [
        "sparse_hash_map.h",
        "sparse_hash_set.h",
        "sparsetable.h"
    ],
    hdrs = [
        "traits.h"
    ],
    deps = [
        "//sparsehash/internal:hash_table_lib"
    ]
)