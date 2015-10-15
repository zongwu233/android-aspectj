This project is an example of how to enable method tracing (which cuts across all classes) in Android.


Adding Aspect to Android


Programming AspectJ with Android

AspectJ is the defacto choice for AOP program. So far I did not see any one trying AOP concept in Android. However, I did read one blog mentioning, it should be possible, hence I tried it.

AspectJ puts in pointcut across code and can execute advices around those pointcuts. The beautify of this is once you compile your java source, you add these pointcuts and advices to your program by injecting them in the byte code (of already generated class files).

Knowing this I knew aspectJ can be used in Android, as dex relies on .class files.

Stage 1- Let Java compile java to .class files

Stage 2- Let AspectJ compiler inject point cuts and advices to the .class files

Stage 3- Let Dex take these new class files and create .dex file.



Read more here - http://blog.punegtug.org/2010/11/adding-aspect-to-android.html

Read more about Maven Integration here - http://code.google.com/p/android-aspectj/wiki/IntegrationwithMaven

**Special thanks to Nikhil Walvekar to come up with Maven Integration**

Nikhil Walvekar - http://www.linkedin.com/in/walvekar