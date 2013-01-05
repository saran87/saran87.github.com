---
layout: post
title: "Serial port communication in windows using java"
date: 2012-08-14
comments: false
categories: [Serial port communication, Java, RXTX library]
---

Serial Port communication using java can be done using RXTX library.&nbsp; RXTX library is a native library provides serial and parallel communication for the Java Development Toolkit (JDK). RXTX is provided under gnu LGPL license. RXTX provides same support as javax.comm library

Installing RXTX in Windows <u>32Bit</u> Machine:
------------------------------------------------
- Identify your Java Runtime Environment's folder. For version 1.6.0, this usually isc:\Program Files\Java\jre1.6.0_01\

- Copy the files from the downloaded RXTX binaries folder. 
Download binaries here [http://rxtx.qbang.org/wiki/index.php/Download](http://rxtx.qbang.org/wiki/index.php/Download)

- Copy rxtxParallel.dll to c:\Program Files\Java\jre1.6.0_01\bin\

- Copy rxtxSerial.dll to c:\Program Files\Java\jre1.6.0_01\bin\

- Copy RXTXcomm.jar to c:\Program Files\Java\jre1.6.0_01\lib\ext\

Installing RXTX in Windows <u>64Bit</u> Machine:
------------------------------------------------
Do the same as for 32 bit except download the binaries from here <a href="http://www.cloudhopper.com/opensource/rxtx/">http://www.cloudhopper.com/opensource/rxtx/</a>

###Using RXTX in Eclipse

Usually RXTX works but for eclipse sometimes it won’t work. You can use below way to 	configure the eclipse environment.

###Way-I:

- Copy RXTXcomm.jar, rxtxSerial.dll and rxtxParallel.dll files to the lib directory of your project
- Under Project | Properties | Java Build Path | Libraries
- Click Add JARs... Button
- Select the RXTXComm.jar from lib directory
- Jar should now be in the Build Path
- expand the RXTXComm.jar entry in the list and select "Native Library Location"
- Select the project lib directory and apply

###Alternative way:

The above setup didn't quite work for me, so here is an alternative.

- Copy RXTXcomm.jar to the lib directory of your project.
- Navigate your package explorer to the lib folder, right click on RXTXcomm.jar | Build Path | Add to build  path.
- Copy rxtxSerial.dll and rxtxParallel.dll files to the root directory of your project.
- Under Run | Run configurations | Classpath tab | User entries | Advanced | Add folder, choose the root folder of your project.

This should be enough just to run it under Eclipse, when deploying a runnable jar, just make sure the dlls are on the same folder as the jar (JVM assumes it for classpath).

###For installing RXTX in Other OS:
Refer this link http://rxtx.qbang.org/wiki/index.php/Installation.

###Usage:
	import gnu.io.*;

The above header file is equivalent to javax.comm and provides all classes and methods provided by it.

	Be careful when using System.in.read() and rxtx in win32; 
	It can trip across a known JRE deadlock bug.

###Samples:

Follow below link for samples given by rxtx.
[Link](http://rxtx.qbang.org/wiki/index.php/Examples)


