# eteran / cpp-utilities / arena / test
cmake_minimum_required(VERSION 3.5)


project("${PROJECT_NAME}-test" CXX)
add_executable("${PROJECT_NAME}" "")


target_sources(
	"${PROJECT_NAME}"
	PRIVATE
		"${CMAKE_CURRENT_LIST_DIR}/Arena.cpp"
)


target_link_libraries(
	"${PROJECT_NAME}"
	PRIVATE
		eteran::cpp-utilities::arena
		eteran::cpp-utilities::defaults
)


add_test("${PROJECT_NAME}" "${PROJECT_NAME}")

