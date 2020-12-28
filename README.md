AArch64 implementation of Chinese SM3 Cryptographic Hash Algorithm. [ch](https://www.oscca.gov.cn/sca/xxgk/2010-12/17/1002389/files/302a3ada057c4a73830536d03e683110.pdf), [en](https://tools.ietf.org/html/draft-sca-cfrg-sm3-02). 

## implementation
* message extension : Neon. 
* compression function : A64.

## build
    $ mkdir build
    $ cd build
    $ cmake ..
    $ make -j
    $ make test

### option
`-DCMAKE_BUILD_TYPE` : possible values are empty, Debug, Release, RelWithDebInfo and MinSizeRel, default is `Release`.  
`-DCMAKE_INSTALL_PREFIX` : where to install fp256 library, default is `/usr/local`.  
`-DBUILD_STATIC` : build static library, default is `ON`.  
`-DBUILD_SHARED` : build shared library, default is `ON`.   
`-DUSE_ASAN` : use AddressSanitizer, default is `OFF`.  

# license
Apache 2.0