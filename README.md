# GCC-installations-steps

This was done in compilers course
This installation of GCC is for the reason that we can link in custom made optimisation routine in GCC compiler

step 1: create a new virtual machine in your virtual box with more than 20 GB space
        This is because the installation takes lot of space
        I made it of 50 GB space.
step 2: google gcc-10.2.0 download or replace the current version
        download the .tar.gz file from a link which looks like indexof/...... something like that
        extract it.
step 3: create two directories named install and objdir in the same directory as your extracted folder from above.
        install ->install directory
        objdir ->build directory
        extracted folder ->source directory.
step 4: install gcc, g++, make in ubuntu using sudo apt install comand
step 5: open gcc source directory in terminal and type the following command
        ./contrib/download_prerequisites
step 6: open build directory in terminal and type the following command replacing the prfix with the path of your install diectory
        ../gcc-10.2.0/configure -enable-languages=c --disable-multilib --enable-install-libiberty --prefix=/home/sagarika/GCC/install/
step 7: after completion of above comand type the following in terminal in the same directory (build directory)
        make
        (beware this step took me about 4 hrs to complete dont let your PC sleep in between)
step 8: open the install directory in the terminal and type 
        make install
        (note: This will add gcc in the install directory specified by "prefix" parameter in step 6)
