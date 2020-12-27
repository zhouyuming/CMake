cmake_minimum_required(VERSION 3.12.1)

project(helloworld)

set(compile_options -Wall -Wcomment)

set(link_flags -Wl,-z,-now -Wl,-z,-noexecstack)

function(myfunc options flags)
    message(STATUS "${options}")
    foreach(option ${options})
        message(STATUS "${option}")
    endforeach()

    message(STATUS "${flags}")
    foreach(flag ${flags})
        message(STATUS "${flag}")
    endforeach()

    list(APPEND options -Werror)
    list(APPEND flags -Wl,-z,relro)
endfunction()

myfunc("${compile_options}" "${link_flags}")

message(STATUS "${compile_options}")
message(STATUS "${link_flags}")