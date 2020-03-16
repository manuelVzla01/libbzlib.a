# libbzlib.a
Explanation of the compilation of the static library in windows libbzlib.a, based on the article Static and Dynamic Libraries | Set 1


Hello, this little explanation helped me to compile the static libbzip2.a library on windows.


first having bzip2 source compile all objects bzlib.o ... etc randtable.o of course with make.

second 

then having all the .o, with this command
ar rcs libbzlib.a bzlib.o blocksort.o crctable.o compress.o decompress.o huffman.o randtable.o


I got the static library. libbzlib.a

And put it in the C: \ MinGW \ lib folder

And from there :
with the application that I'm doing
gcc.exe -lbzlib -oexe


I was able to resolve these errors:
undefined reference to `BZ2_bzDecompress@4'
undefined reference to `BZ2_bzDecompressEnd@4'



I have the library for those who want to use it.
Thank you
