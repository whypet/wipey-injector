# WipeyInjector
wipet's fun dll injector
creds to nullexception
uses CreateRemoteThread() & RtlCreateUserThread() undocumented api function
tested on command prompt, notepad and minecraft (java)
anyone can use this code without my permission in a program

# how it works
it adjusts the debug privilege token, then creates a handle to the process to inject the dll to using a PID (process ID),
which is later used to write allocated memory for the dll path into the process and to inject the dll into the process
using CreateRemoteThread(). if it fails, it tries to use RtlCreateUserThread()
at the end of the function, it returns the injected dll thread's exit code