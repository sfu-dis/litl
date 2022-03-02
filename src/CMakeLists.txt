set(LITL_MCS_SRC
  ${CMAKE_CURRENT_SOURCE_DIR}/mcs.c
  ${CMAKE_CURRENT_SOURCE_DIR}/utils.c
)
add_library(litl_mcs ${LITL_MCS_SRC})
target_compile_definitions(litl_mcs PUBLIC WAITING_SPIN_THEN_PARK FCT_LINK_SUFFIX=mcs)

set(LITL_TTAS_SRC
  ${CMAKE_CURRENT_SOURCE_DIR}/ttas.c
  ${CMAKE_CURRENT_SOURCE_DIR}/utils.c
)
add_library(litl_ttas ${LITL_TTAS_SRC})
target_compile_definitions(litl_ttas PUBLIC WAITING_ORIGINAL FCT_LINK_SUFFIX=ttas)
