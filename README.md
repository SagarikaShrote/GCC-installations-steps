# GCC-installations-steps

This was done in compilers course <br>
This installation of GCC is for the reason that we can link in custom made optimisation routine in GCC compiler <p>

step 1: create a new virtual machine in your virtual box with more than 20 GB space <br>
        This is because the installation takes lot of space <br>
        I made it of 50 GB space. <p>
step 2: google gcc-10.2.0 download or replace the current version <br>
        download the .tar.gz file from a link which looks like indexof/...... something like that <br>
        extract it. <p>
step 3: create two directories named install and objdir in the same directory as your extracted folder from above. <br>
        install ->install directory <br>
        objdir ->build directory <br>
        extracted folder ->source directory. <p>
step 4: install gcc, g++, make in ubuntu using sudo apt install comand <p>
step 5: open gcc source directory in terminal and type the following command <br>
        ./contrib/download_prerequisites <p>
step 6: open build directory in terminal and type the following command replacing the prfix with the path of your install diectory <br>
        ../gcc-10.2.0/configure -enable-languages=c --disable-multilib --enable-install-libiberty --prefix=/home/sagarika/GCC/install/ <p>
step 7: after completion of above comand type the following in terminal in the same directory (build directory) <br>
        make <br>
        (beware this step took me about 4 hrs to complete dont let your PC sleep in between) <p>
step 8: in the same directory (objdir), in the terminal, type <br>
        make install <br>
        (note: This will add gcc in the install directory specified by "prefix" parameter in step 6) <br>
