project('test', 'fortran')

fortran_args = []
if get_option('C2')
    fortran_args += '-DC2'
endif

test_lib = static_library('test1', 'src/kinds.F90', fortran_args: [fortran_args])  # This is the problem: `fortran_args: ['']`

exe = executable('test2', 'src/main.f90',
    link_with: [test_lib])
