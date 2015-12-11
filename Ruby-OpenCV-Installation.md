
#如何安装Ruby-OpenCV

   主要参考的文章是：[Install OpenCV 2.4.10 in Ubuntu 14.04LTS 64-bit][1]
   其中第五步的代码应该改为
```
    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D BUILD_NEW_PYTHON_SUPPORT=ON -D WITH_V4L=ON -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=ON -D WITH_OPENGL=ON .  
    make -j $(nproc) # Use multiple processes if available  
    sudo make install
```
   > 要点是在CMAKE的ON后面输入.，而不是..，否则就会让CMAKE认为是编译上级目录。
   > 另外，Ubuntu 14.04 LTS 64-bit操作系统要安装libgtk2.0-dev和pkg-config之后再进行编译。
[1]: http://codentricks.com/2015/05/install-opencv-2-4-10-in-ubuntu-14-04lts-64-bit/   


