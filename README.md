# mkjail
This contains a script I wrote (```mkjail```) to create chroot jails on Mac OS
X. It works for me on Mac OS X 10.10.5.

I also include a helper script (```recurse```) which recursively calls ```otool
-L``` to find the shared library dependencies of an executable.

The ```mkjail.files``` file contains paths of files to be copied to the jail.
The ```addtojail``` script can be used to easily add a new executable to that
file, which will include it in future ```mkjail``` executions. It calls
```recurse``` to ensure that all shared libraries it depends upon (directly or
indirectly) are also added.
