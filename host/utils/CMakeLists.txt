########################################################################
# Build and Install the UmTRX utils
########################################################################
INSTALL(PROGRAMS
    umtrx_net_burner
    umtrx_cal_tx_dc_offset
    DESTINATION bin
)

add_executable(umtrx_test_chains umtrx_test_chains.cpp)
target_link_libraries(umtrx_test_chains ${UMTRX_LIBRARIES})
install(TARGETS umtrx_test_chains DESTINATION bin)
