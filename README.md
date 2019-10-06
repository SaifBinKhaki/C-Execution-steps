# C-Execution-steps
Before Coming to execution, lets discuss some compilers of C, C++ and objective C. There are a lot providing services, a few of them are GCC, visual studio etc. Lets discuss GCC,

GCC = GNU Compiler Collection (It has all the compilers in it for all the processes till execution.)
GNU = GNU's Not Unix (UNIX is an operating system. GNU is a system that allocates machine resources and talks to the hardware through kernel for example LINUX/kernel.)

Now we have compilers for compiling, now we will see how much we can interact to an hardware through a specific OS.
Kernels: It is actually an interface between user mode and physical hardware.
There are three types of Kernels:

MICRO-KERNEL:

It allows access to CPU,memory and IPC (inter processes communication) but in this kernel, all the processes run in queue. OS: OS X

MONO-LETHIC KERNEL:

It allows most of the access to the user mode that is why is less secure but have better IPS and large memory footprint. This provides a more direct access to the hardware components like CPU, Memory, IPC, Drivers and server calls. It has an advantage that the processes dont run in queue so the processes dont have to wait for one process to complete. OS: LINUX/KERNEL

HYBRID-KERNEL:

Kernels can decide what hardwares they want to be in user mode and what in supervisor mode. Drivers and i/o are provided in USER MODE while IPC and server calls are in SUPERVISOR MODE.

        --What is a memory footprint?--
        --It is actually the amount memory used or referenced by a program while running.--

There are usually four steps for a file to execute properly with an extension of c or cpp.

Lets suppose we have a file name practice.c 

1.PREPROCESSING
        Since compiling is called PROCESSING. We would name this step as, PREPROCESSING. Even before compiler can start its work, our cpp program module is firstly directed to the preprocessor through preprocessor directives. in { #include, preprocessor directive }, # is the preprocessor symbol which are converted at the preprocessing stage. include is instructing the preprocessor to paste all the code from <> or "" files in present cpp module. Now, the preprocessor has converted the .c file to .i file (.ii if .cpp).
        
2.COMPILING
        This is where a compiler gets to see the code. Compiler will see calls to functions and picks references and convert the preprocessed code to assembly code. This is the point where any compiler throws compile time errors because it can't convert the code into assembly code according to its rules specified.
          
          --What really is an assembly code?--
          --Assembly code is the human readable coding language with one-to-one contact between human and machine.--
After the code is converted to assembly code, its extension is changed to .s This is the stage where assembly code is converted into object code with file having extension .o
          
          --What really is an object code?--
          --Object code is the necessary machine coding which must be there with a program's machine code to run. This necessary coding has offsets and placeholders that are used by linkers to link all the files together.--

3.LINKING
        Linker as discussed above, links all the files from their placeholders and offsets and will produce one executable file with .exe extension. These exe files are fully written in binary machine code. Actually links all the object codes and library files needed to run the program.

4.LOADING
        It loads the exe file inm ain or primary memory and the program runs or (for the you were searching this far) executes.

          --Then what really is an interpreter?and why we didnt need it in this execution processes?--
          --Interpreters are the compilers but with different execution method. Compilers turn source code file to machine code file and then executes the compilete file. However, interpreters take one statement and convert it into machine code and then execute it. Then with an iteration, does the same with all the other statements. This thing helps a lot when writing a large program. Languages that use interpreters are JAVA, C#, Perl, javascript etc.--
          
          --What is a Script? What is script in JAVAScript?--
          --Scripting is the process of executing the file without even compiling. It may be called as interpreting without compiling. Such languages which need not any compiling are called Scripting languages. For exampe Javascript-- 
