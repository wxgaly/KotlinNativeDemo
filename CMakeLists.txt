cmake_minimum_required(VERSION 3.8)

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_LIST_DIR}/KotlinCMakeModule)

project(KotlinNativeDemo1 Kotlin)

cinterop(
    NAME CInterop
    DEF_FILE null.def
    COMPILER_OPTS -Isrc/c -IE:/code/github/KotlinNativeDemo1/src/main/c)

konanc_executable(
    NAME Main
    SOURCES src/main/kotlin/Main.kt)

