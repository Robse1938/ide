# Building the Amzi! IDE Eclipse Plug-in

## History

The Eclipse plug-in was developed around 2002 by Amzi! developer Mary Kroening.  It was the first Eclipse IDE for Prolog code that included a colorized editor, cross reference capability, and most important a full four-port debugger that highlights lines of code as Prolog goes through it's backtracking search.  The debugger also keeps windows open with the full stack trace and variable bindings.

The debugger works in conjunction with Prolog code that runs in debug mode.  Understand that much of Prolog is written in Prolog, so for example Prolog listeners are often written in Prolog.  In the case of Amzi! the Prolog debugger is written in Prolog.  It communicates via the Amzi! Java interface with Eclipse, providing information about the current line of code, status, call stack, etc.

Mary has since passed away, cancer.  She was the force behind much of the outward appearance of Amzi! Prolog + Logic Server, such as the Eclipse IDE, and a major contributor to the World-wide popularity of the software.

I have re-built the IDE a couple of times, but always find Eclipse RCP to be extremely brittle.  It is basically unchanged from that 2002 version.  The build reflected in the first github version supports building the plug-in, but not the full RCP stand-alone IDE.  I believe this might be best for open source anyway as it appears to work across platforms, running at least on both a Mac and Windows.

I welcome more experienced Eclipse developers to work with the IDE plug-in and bring it up to date with current Eclipse best practices.

## Building

1. Download and install Eclipse 4.5.1 for plug-in development.
2. Rebuild all
3. Open com.amzi.prolog-update_site
4. delete all the jar files in features, plugins and both artifacts.jar and content.jar
5. Rebuild all
6. Copy the new files in com.amzi.prolog-update_site to a new location, and it is the new plug-in.

## Running

1. Download and install any version of Eclipse.
2. Make sure the Amzi! *apls* directory is in the correct relative place compared to the Eclipse executable:

```
eclipse
  eclipse.app/exe whatever
apls
  bin
  lib
  ...
```
3. If you are running Windows, you can set the environment variable AMZI_DIR to point to the amzi\apls directory and then you don’t need to maintain the relative paths above.
4. Import the plug-in and maybe it will work!

--Dennis




