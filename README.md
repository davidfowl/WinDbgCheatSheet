WinDbg Cheat Sheet
==================

```
!loadby sos clr
```

Loads the sos extension (lets you run commands on managed code)

```
kv
```

Show the stack on the current thread's stack (mixed managed/unmanaged)

```
~*kv
```

Show the stack of all threads (mixed managed/unmanaged)


```
!dumpheap -stat
```

Dumps the heap

```
!dumpheap -type {typename}
```

Dumps all objects that match the type name (partial matches)

```
!do {address}
```

Dump object

```
!gcroot {address}
```

Show all objects that hold onto the object at address

```
!dso
```

Dump stack objects

```
.preferdml 1
```

Makes everything hyperlinks!

```
sxe clr
```

Break on first chance CLR exceptions.

```
sxd -c "!pe" clr
```

Print the details of every CLR exception as it occurs _without_ breaking into the debugger.

```
!EEStack -EE
```

Dumps the managed stack of every managed thread in the process.

```
dv
```

Dump native variables on the current frame.

```
!exchain
```

Show all exception handlers on the stack.

```
.lastevent
```

Shows what the hell happened on the thread.


```
!gle
```

Get the last error on the current thread.

```
~*e {command}
```

Runs command on each thread.

```
!runaway
```

Shows the time the threads have been running

```
.shell ci {command}
```

Open shell for command execution

