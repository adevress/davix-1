


file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/build/html/")
addDoxyGeneration("Doxyfile.in")
SET( l_doc "${CMAKE_CURRENT_BINARY_DIR}/build/html/")

install(DIRECTORY ${l_doc}
		DESTINATION ${DOC_INSTALL_DIR}/html/) # install examples 


FILE(GLOB man1_page ${CMAKE_CURRENT_SOURCE_DIR}/man/*.1)
install(FILES ${man1_page}
                        DESTINATION ${MAN_INSTALL_DIR}/man1/)
                        
FILE(GLOB man3_page ${CMAKE_CURRENT_SOURCE_DIR}/man/*.3)
install(FILES ${man3_page}
                        DESTINATION ${MAN_INSTALL_DIR}/man3/)                        
                        
                        
                        

