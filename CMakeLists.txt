cmake_minimum_required(VERSION 2.8)	 # Проверка версии CMake.
										# Если версия установленой программы
										# старее указаной, произайдёт аварийный выход.

project(hello_world)			# Название проекта

add_library(
	hello 
	STATIC 
	hello.cpp
)	# Создание статической библиотеки с именем hello

add_executable(
	main 
	main.cpp
)	# Создает исполняемый файл с именем main

target_link_libraries(main hello)		# Линковка программы с библиотекой
