# Quiz questions
   ## Question #0
        What are the steps of compilation?


       [] compiler 2. preprocessor 3. assembler 4. linker

       [x] preprocessor 2.compiler 3. assembler 4. linker

       [] preprocessor 2.compiler 3. linker 4. assembler
    
   ## Question #1
        The preprocessor generates assembly code


       [] True

       [x] False

   ## Question #2
        The preprocessor generates object code


       [] True


       [x] False

   ## Question #3
        The preprocessor links our code with libraries.


       [] True


       [x] False

   ## Question #4
        This portion of code is actually using the library stdlib.

        #include <stdlib.h>

       [] True


       [x] False

   ## Question #5
        The preprocessor removes all comments


       [x] True


       [] False

   ## Question #6
        What is the gcc option that runs only the preprocessor?


       [] -a


       [] -P


       [] -p


       [] -pedantic


       [x] -E


       [] -cisfun


       [] -preprocessor

   ## Question #7
        NULL is a macro


       [x] True


       [] False

   ## Question #8
        What will be the last 5 lines of the output of the command gcc -E on this code?

        #include <stdlib.h>

       [] int main(void)
            {
                NULL;
                return (EXIT_SUCCESS);
            }

       [] int main(void)
            {
            0;
            return (0);
            }

       [] int main()
            {
            0;
            return (0);
            }

       [x] int main(void)
            {
            ((void *)0);
            return (0);
            }

       [] int main(void)
            {
            '\0';
            return (0);
            }
   ## Question #9
        This code will try to allocate 1024 bytes in the heap:

        #define BUFFER_SIZE 1024
        malloc(BUFFER_SIZE)

       [x] True


       [] False

   ## Question #10
        What does the macro TABLESIZE expand to?

        #define BUFSIZE 1020
        #define TABLESIZE BUFSIZE
        #undef BUFSIZE
        #define BUFSIZE 37

       [] 1020


       [x] 37


       [] nothing

   ## Question #11
        This is the correct way to define the macro SUB:

        #define SUB(a, b) a - b

       [] Yes


       [] No, it should be written this way:

            #define SUB(a, b) (a - b)

       [] No, it should be written this way:

            #define SUB(a, b) (a) - (b)

       [x] No, it should be written this way:

            #define SUB(a, b) ((a) - (b))
   ## Question #12
        Why should we use include guards in our header files?


            [] Because we said so, and we should never ask why.


            [x] To avoid the problem of double inclusion when dealing with the include directive.

   ## Question #13
        The macro __FILE__ expands to the name of the current input file, in the form of a C string constant.


             [x] True


             [] False

   ## Question #14
        What will be the output of this program? (on a standard 64 bits, Linux machine)

        #include <stdio.h>
        #include <stdlib.h>

        #define int char

        int main(void)
        {
            int i;

            i = 5;
            printf ("sizeof(i) = %lu", sizeof(i));
            return (EXIT_SUCCESS);
        }

           [] Segmentation Fault


           [] It does not compile


           [] sizeof(i) = 8


           [] sizeof(i) = 5


           [] sizeof(i) = 4


           [x] sizeof(i) = 1