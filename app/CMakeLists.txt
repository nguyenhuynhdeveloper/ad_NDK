cmake_minimum_required(VERSION 3.10.2)

project("adndk")

add_library( # Tên thư viện của bạn
             native-lib

             # Tạo thư viện từ các file mã nguồn
             SHARED

             # Thêm các file .cpp vào đây
             src/main/cpp/native-lib.cpp)

find_library( # Tìm thư viện log
              log-lib
              log )

target_link_libraries( # Liên kết thư viện với NDK log
                       native-lib
                       ${log-lib} )
