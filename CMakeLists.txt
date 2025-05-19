add_library(SMAA INTERFACE)

target_include_directories(SMAA INTERFACE
  include
)

file(GLOB_RECURSE SMAA_HLSL
  SMAA.hlsl
)

target_compile_definitions(SMAA INTERFACE
  SMAA_HLSL="$<JOIN:${SMAA_HLSL},;>"
)