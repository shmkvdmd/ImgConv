# Добавляем исходные файлы проекта
set(SOURCES
    main.cpp
    image.cpp
    ppm_image.cpp
    ico_image.cpp
    tiff_image.cpp
    bmp_image.cpp
    png_image.cpp
    jpeg_image.cpp
)

# Добавляем заголовочные файлы проекта
set(HEADERS
    image.h
    ppm_image.h
    ico_image.h
    tiff_image.h
    bmp_image.h
    png_image.h
    jpeg_image.h
    pack_defines.h
)

# Добавляем исполняемый файл
add_executable(ImgConv ${SOURCES} ${HEADERS})

# Линкуем библиотеки
target_link_libraries(ImgConv PRIVATE "${JPEG_LIBRARY}" "${PNG_LIBRARY}")

# Устанавливаем пути к заголовочным файлам
target_include_directories(ImgConv PRIVATE "${JPEG_INCLUDE_DIR}" "${PNG_INCLUDE_DIR}")