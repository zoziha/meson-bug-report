project('test', 'fortran')

C2 = get_option('C2')
if C2
    C2_macro = '-DC2'
else
    C2_macro = ''
endif

test_lib = static_library('test1', 'src/kinds.F90', fortran_args: [C2_macro])  # This is the problem: `fortran_args: ['']`

exe = executable('test2', 'src/main.f90',
    link_with: [test_lib])
