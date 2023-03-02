
 # Portable UnRAR version #


 ###  1. General ###

   This package includes UnRAR's C++ source-code and ```makefile``` for
   several Unix / Linux-oriented compilers.

   UnRAR is a subset of RAR and generated from RAR's source automatically
   by a small program removing blocks like:
   
   ```#ifndef UnRAR
   /* ... */
   #endif```
   

  This method is not perfect and you may find some RAR related stuff
   unnecessary in UnRAR, Especially in the header files.

   If you wish to port UnRAR to a new platform, you may need to edit:
   
   ```#define LITTLE_ENDIAN```` in ```OS.hpp``` as well as the data type definitions
   data type definitions found in ```rartypes.hpp```

   If the computer architecture does not allow not aligned data access,
   you need to undefine ```ALLOW_NOT_ALIGNED_INT```and define
   ```STRICT_ALIGNMENT_REQUIRED```in ```OS.h```

   ```UnRAR.vcproj``` and ```UnRARDll.vcproj``` are built using Microsoft Visual C++
   
   ```UnRARDll.vcproj``` builds the ```UnRAR.dll``` Dynamic Link library.


 ###  2. Unrar binaries ###

   If you compiled UnRAR for an OS which is not present in "Downloads"
   and "RAR extras" on https://rarlab.com we would appreciate it if you could send
   us the compiled executable to place it to our site.


###   3. Acknowledgements ###

   This source-code includes parts of code written by other people.

   Please see ```acknow.txt``` file for more information.


$##  4. Legal garbage you shouldn't waste time reading ###

   UnRAR's source-code may be used in any software to handle .RAR archives
   without limitations free of charge, but cannot be used to re-create
   the RAR compression algorithm, which is proprietary. Distribution
   of modified UnRAR source in separate form or as a part of other
   software is permitted, provided that it is clearly stated in
   the documentation and source comments that the code may not be used
   to develop a RAR (WinRAR) compatible archiver.

   More detailed licensing bullshit is available in ```license.txt```
