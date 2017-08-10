---
layout: default
title: "Resources"
---

This page contains links to useful resources.

-   [Visual Studio 2015](https://e5.onthehub.com/WebStore/ProductsByMajorVersionList.aspx?cmi_cs=1&cmi_mnuMain=bdba23cf-e05e-e011-971f-0030487d8897&ws=c1ca0b0c-0f62-e511-9410-b8ca3a5db7a1&vsro=8) is available through MSDNAA.
-   [FreeGLUT](http://freeglut.sourceforge.net/) the OpenGL window management package we will be using. The package is targetted to Linux, but you can get a distribution for [Windows](http://www.transmissionzero.co.uk/software/freeglut-devel/) (this package will also work on VS 2013).
-   [SOIL](http://www.lonesock.net/soil.html) the Simple OpenGL Image Library package we will be using. I have precompiled libraries for Windows and Mac OSX that can be downloaded in the corresponding installation section below.
-   [GLEW](http://glew.sourceforge.net/) the OpenGL Extension Wrangler Library package we will be using for shaders (since Windows contains an old version of OpenGL). NOTE: OSX contains a current version of OpenGL and thus does not require GLEW.

FreeGLUT Installation Instructions
----------------------------------

**Windows 8.1 (Visual Studio 2015)**

1.  Open Visual Studio 2015. Select **File->New->Project**. Under the **Templates** tab expand **Other Languages**. Select **Visual C++**. Select **Install Visual C++ 2015 Tools for Windows Desktop**. Follow the installation procedure to setup the necessary Windows SDK.

2.  Download and extract [freeglut 3.0.0 MSVC Package](http://www.transmissionzero.co.uk/software/freeglut-devel/).

3.  Copy the contents of the **include\\GL** directory to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

4.  Copy **freeglut.lib** from the **lib** directory (**NOT** the x64 subdirectory) to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

5.  Copy **freeglut.dll** from the **bin** directory (**NOT** the x64 subdirectory) to:

    - C:\\Windows\\SysWOW64

**Windows 10 (Visual Studio 2015)**

1.  Open Visual Studio 2015. Select **File->New->Project**. Under the **Templates** tab expand **Other Languages**. Select **Visual C++**. Select **Install Visual C++ 2015 Tools for Windows Desktop**. Follow the installation procedure to setup the necessary Windows SDK.

2.  Download and extract [freeglut 3.0.0 MSVC Package](http://www.transmissionzero.co.uk/software/freeglut-devel/).

3.  Copy the contents of the **include\\GL** directory to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

4.  Copy **freeglut.lib** from the **lib** directory (**NOT** the x64 subdirectory) to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

5.  Copy **freeglut.dll** from the **bin** directory (**NOT** the x64 subdirectory) to:

    - C:\\Windows\\SysWOW64

**Linux (ubuntu)**

From a terminal window

```cpp
$ sudo apt-get install freeglut3-dev
```

**Mac OSX**

Install **XCode** from the App Store. 

Then in a terminal window 

```cpp
$ sudo xcode-select --install
```

to install the command line tools.

SOIL Installation Instructions
------------------------------

**Windows 8.1 (Visual Studio 2015)**

1.  Copy the header file [SOIL.h](soil/win64/SOIL.h) to (you will need to make a new **SOIL** directory):

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\SOIL

2.  Copy the library [SOIL.lib](soil/win64/SOIL.lib) to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

**Windows 10 (Visual Studio 2015)**

1.  Copy the header file [SOIL.h](soil/win64/SOIL.h) to (you will need to make a new **SOIL** directory):

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\SOIL

2.  Copy the library [SOIL.lib](soil/win64/SOIL.lib) to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

**Linux (ubuntu)**

From a terminal window

```cpp
$ sudo apt-get install libsoil-dev
```
	
**Mac OSX**

1.  Download the [mac header](soil/mac/SOIL.h).

2.  In a terminal window, from the directory where you downloaded the header file:

	```cpp
	$ sudo mkdir /usr/local/include/SOIL
	
	$ sudo cp SOIL.h /usr/local/include/SOIL/
	```

3.  Download [libSOIL.a](soil/mac/libSOIL.a).

4.  In a terminal window, from the directory where you downloaded the library:

	```cpp
	$ sudo cp libSOIL.a /usr/local/lib/
	```
	
GLEW Installation Instructions
------------------------------

**Windows 8.1 (Visual Studio 2015)**

1.  Download and extract (be sure to get the Windows 32-bit version even if you are running a 64-bit OS) [precompiled binaries](https://sourceforge.net/projects/glew/files/glew/2.0.0/glew-2.0.0-win32.zip/download).

2.  Copy the contents of the **include\\GL** directory to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

3.  Copy **glew32.lib** in the **lib\\Release\Win32** directory to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

4.  Copy **glew32.dll** in the **bin\Release\Win32** directory to:

    - C:\\Windows\\SysWOW64

**Windows 10 (Visual Studio 2015)**

1.  Download and extract (be sure to get the Windows 32-bit version even if you are running a 64-bit OS) [precompiled binaries](https://sourceforge.net/projects/glew/files/glew/2.0.0/glew-2.0.0-win32.zip/download).

2.  Copy the contents of the **include\\GL** directory to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

3.  Copy **glew32.lib** in the **lib\\Release\Win32** directory to:

    - C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

4.  Copy **glew32.dll** in the **bin\Release\Win32** directory to:

    - C:\\Windows\\SysWOW64

**Linux (ubuntu)**

From a terminal window

```cpp
$ sudo apt-get install libglew-dev
```

**Mac OSX**

GLEW is not needed for OSX.
