1) *Del paso pre-procesador: pero que procese las directivas # del calculator.c y que al hacerlo, como este contiene un include calculator.h procese también las de éste. 

   *Del paso Compilación 1 espero que realice un análisis sintáctico, semántico y léxico, genere una intermediante representación (IR) y la optimice, y por último que me cree un archivo en assembler con la información del código y realice optimizaciones de hardware.

   *Del Compilador 2 espero que genere los objetos en binario  
   
   *Del linkeo espero que al objeto que esta en binario lo vuelva ejecutable 


2) En el calculator.pp.c creado por el pre-procesador vemos unidos el código del calculator.c y el del calculator.h, es decir, en lugar de tener el #include "calculator.h" al comienzo del codigo ahora lo tenemos explìcitamente. Ademàs agregò todos los comandos que utiliza el stdio.h (que venia del compilator.h) que utiliza en el procesador. 

3) Las funciones en el calculator.asm siguen siendo el main y addnumbers, pero ahora estàn escritas en términos de las instrucicones del assembler: call,movel,leave, addl, etc

4) Los simbolos que se crean en el objeto 

000000000000003c T add_numbers
0000000000000000 T main
                 U printf

U significa que el símbolo no está definido
T significa que el símbolo esta en el código 

Como ambos están en mayúscula son globales

(LO TERMINO DESPUÉS)

5) PEGO AHORA TODO ESTO PARA ANALIZAR Y HACER LAS RESPUESTAS DESPUÉS  


0000000000400562 T add_numbers
0000000000601038 B __bss_start
0000000000601038 b completed.7594
0000000000601028 D __data_start
0000000000601028 W data_start
0000000000400460 t deregister_tm_clones
00000000004004e0 t __do_global_dtors_aux
0000000000600e18 t __do_global_dtors_aux_fini_array_entry
0000000000601030 D __dso_handle
0000000000600e28 d _DYNAMIC
0000000000601038 D _edata
0000000000601040 B _end
00000000004005f4 T _fini
0000000000400500 t frame_dummy
0000000000600e10 t __frame_dummy_init_array_entry
0000000000400778 r __FRAME_END__
0000000000601000 d _GLOBAL_OFFSET_TABLE_
                 w __gmon_start__
000000000040062c r __GNU_EH_FRAME_HDR
00000000004003c8 T _init
0000000000600e18 t __init_array_end
0000000000600e10 t __init_array_start
0000000000400600 R _IO_stdin_used
                 w _ITM_deregisterTMCloneTable
                 w _ITM_registerTMCloneTable
0000000000600e20 d __JCR_END__
0000000000600e20 d __JCR_LIST__
                 w _Jv_RegisterClasses
00000000004005f0 T __libc_csu_fini
0000000000400580 T __libc_csu_init
                 U __libc_start_main@@GLIBC_2.2.5
0000000000400526 T main
                 U printf@@GLIBC_2.2.5
00000000004004a0 t register_tm_clones
0000000000400430 T _start
0000000000601038 D __TMC_END__

