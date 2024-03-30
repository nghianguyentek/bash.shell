# Base Builtin `ulimit`

*Control provided resources of started-by-shell processes*

## Synopsis

```bash
ulimit [-HS] -a
ulimit [-HS] [-bcdefiklmnpqrstuvxRT] [limit]
```

If `limit` is given, and the [-a](#-a) option is not used, `limit` is the new value of the specified resource. The special limit values hard, soft, and unlimited stand for the current hard limit, the current soft limit, and no limit, respectively. A hard limit cannot be increased by a non-root user once it is set; a soft limit may be increased up to the value of the hard limit. Otherwise, the current value of the soft limit for the specified resource is printed, unless the [-H](#-h) option is supplied. When more than one resource is specified, the limit name and unit, if appropriate, are printed before the value. When setting new limits, if neither [-H](#-h) nor [-S](#-s) is supplied, both the hard and soft limits are set. If no option is given, then [-f](#-f) is assumed. Values are in 1024-byte increments, except for [-t](#-t), which is in seconds; [-R](#-r), which is in microseconds; [-p](#-p), which is in units of 512-byte blocks; [-P](#-p-1), [-T](#-t-1), [-b](#-b), [-k](#-k), [-n](#-n) and [-u](#-u), which are unscaled values; and, when in POSIX Mode (see Bash POSIX Mode), [-c](#-c) and [-f](#f), which are in 512-byte increments.

The return status is zero unless an invalid option or argument is supplied, or an error occurs while setting a new limit.

## Options

### `-a`

All current limits are reported; no limits are set.

### `-b`

The maximum socket buffer size.

### `-c`

The maximum size of core files created.

### `-d`

The maximum size of a process’s data segment.

### `-e`

The maximum scheduling priority ("nice").

### `-f`

The maximum size of files written by the shell and its children.

### `-i`

The maximum number of pending signals.

### `-k`

The maximum number of kqueues that may be allocated.

### `-l`

The maximum size that may be locked into memory.

### `-m`

The maximum resident set size (many systems do not honor this limit).

### `-n`

The maximum number of open [file descriptors](https://github.com/nghianguyentek/unix.os/blob/main/file-descriptor.md) (most systems do not allow this value to be set).

### `-p`

The pipe buffer size, in units of 512-byte blocks.

### `-q`

The maximum number of bytes in POSIX message queues.

### `-r`

The maximum real-time scheduling priority.

### `-s`

The maximum stack size.

### `-t`

The maximum amount of cpu time in seconds.

### `-u`

The maximum number of processes available to a single user.

### `-v`

The maximum amount of virtual memory available to the shell, and, on some systems, to its children.

### `-x`

The maximum number of file locks.

### `-H`

Change and report the hard limit associated with a resource.

### `-P`

The maximum number of pseudoterminals.

### `-R`

The maximum time a real-time process can run before blocking, in microseconds.

### `-S`

Change and report the soft limit associated with a resource.

### `-T`

The maximum number of threads.