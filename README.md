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
