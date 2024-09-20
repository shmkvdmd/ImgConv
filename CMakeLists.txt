cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 20)
project(ImgConv)

# Устанавливаем путь к vcpkg
set(CMAKE_TOOLCHAIN_FILE "C:/Users/traru/vcpkg/scripts/buildsystems/vcpkg.cmake")

# Указываем пути к библиотекам и заголовочным файлам
set(JPEG_INCLUDE_DIR "C:/Users/traru/vcpkg/installed/x64-windows/include")
set(JPEG_LIBRARY "C:/Users/traru/vcpkg/installed/x64-windows/lib/jpeg.lib")
set(PNG_INCLUDE_DIR "C:/Users/traru/vcpkg/installed/x64-windows/include")
set(PNG_LIBRARY "C:/Users/traru/vcpkg/installed/x64-windows/lib/libpng16.lib")

# Добавляем поддиректорию lib
add_subdirectory(lib)