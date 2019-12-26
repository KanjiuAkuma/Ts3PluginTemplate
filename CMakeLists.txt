set(CMAKE_CXX_STANDARD 20)

set(TS3_FILES
    include/teamlog/logtypes.h
    include/teamspeak/clientlib_public_definitions.h
    include/teamspeak/public_definitions.h
    include/teamspeak/public_definitions_rare.h
    include/teamspeak/public_errors.h
    include/teamspeak/public_errors_rare.h
    include/plugin_definitions.h
    include/ts3_functions.h
    )

add_library(TS3_BASE STATIC ${TS3_FILES})
set_target_properties(TS3_BASE PROPERTIES LINKER_LANGUAGE CXX)
target_include_directories(TS3_BASE PUBLIC include)