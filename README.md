# HowToBuildGCAM
 
# Build instructions
   > http://jgcri.github.io/gcam-doc/gcam-build.html

# 3+1 libraries (Hector)
    
    ![avatar](https://github.com/heishanmao/HowToBuildGCAM/raw/master/pic/1.png)
    
## Building third party libraries
   1. Boost
   
        VS 2019自带工具 Developer Command Prompt for VS 2019 （管理员运行）
        
        >cd <GCAM Workspace>/libs/boost-lib 
        
        >bootstrap.bat 
        
        >b2 --with-system --with-filesystem address-model=64 stage
        
   2. Xerces
        
        * 解压xerces-c-3.2.3，进入解压后目录
           >mkdir build
           
           >cd build

           >cd ..
                                                                                                 
           >cmake -G "Visual Studio 16 2019" -DCMAKE_INSTALL_PREFIX=<GCAM Workspace>\xercesc .（这一步用cmake –help可以查看可用的VS版本
                                                                                                 
           >cmake --build . --config Debug
                                                                                                                                                                                                                                                                                                                                                                                                                                                 
           >ctest -V -C Debug -j 4                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
           
           >cmake --build . --config Debug --target install
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
        *  Copy <GCAM Workspace>\libs\xercesc\bin\xerces-c_3_2D.dll to <GCAM Workspace>\exe
   
   3. Java
   
   Java 的安装目录找到 copy到 &lt; GCAM Workspace &gt; \libs中
   
   >libs/java/include/jni.h 
   >libs/java/include/jni_md.h 
   >libs/java/lib/jvm.lib
            