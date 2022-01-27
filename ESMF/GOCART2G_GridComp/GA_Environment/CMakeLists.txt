esma_set_this ()

esma_add_library (${this}
  SRCS ${this}Mod.F90
  DEPENDENCIES MAPL Chem_Shared2G Process_Library
  )

if (NOT CMAKE_Fortran_COMPILER_ID MATCHES "NAG")
   target_link_libraries(${this} PRIVATE OpenMP::OpenMP_Fortran)
endif ()
