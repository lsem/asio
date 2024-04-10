cmake_minimum_required(VERSION 3.5)

add_library(asio INTERFACE)
add_library(asio::asio ALIAS asio)

target_include_directories(asio INTERFACE asio/include)
target_compile_definitions(asio INTERFACE ASIO_STANDALONE)

install(DIRECTORY asio/include/asio DESTINATION include/)
