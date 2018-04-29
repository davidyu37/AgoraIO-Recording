1. Introduction to Java Demo:
 The Java Demo provides the Java API for recording.
 The Java API is an encapsulation of the C++ API for recording, ‘samples/agorasdk’, which shares C++ sample code and provides API and callbacks of recording native SDK. You can call the native interfaces with Java through JNI proxy.
    
2. Prepare Java Environment:
 Please make sure your Java environment is ready, for example, you can compile and run hello world.

3. Build Java Demo:
 a. Set JNI path and make CLASSPATH and LD_LIBRARY_PATH in effect: run ‘source build.sh pre_set xxxx’, in which ‘xxx’ is the absolute path of ‘jni.h’. To find the absolute path of ‘jni.h’, you can run ‘locate jni.h’ or ‘find /usr -name jni.h’.
 b. Build Java Demo: run ‘./build.sh build’. 
 c. Clear Java Demo: run ‘./build clean’. 

Note:
 a. The pre-set command sets LD_LIBRARY_PATH and CLASSPATH to ‘bin’. The setting is only effective for the current window. To make the setting effective for other windows, you can run the pre-set command again or make the setting global.
 a. The build command generates ‘bin/librecording.so’. It is a dynamic library file encapsulating ‘samples/agorasdk’. You can call the native interfaces with Java through JNI proxy.
 b. The clear command deletes the .so, .class, and .h files in directory ’bin/‘.