WinDbg Cheat Sheet
==================

```
!loadby sos clr
```

Loads the sos extension (lets you run commands on managed code)

```
kv
```

Show the stack on the current thread's stack

```
~*kv
```

Show the stack of all threads

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
