# notmuch

### installation:
```sh
$ cc -O3 -Wall notmuch.c -o notmuch
```
Optimization is critical for maximum performance on all platforms.  "-o" flag required for newer XCode versions.

### usage:
```sh
$ ./notmuch [arg ...]
```
### what's it do?
not much

### troubleshooting...
please read the fine manual (this) thoroughly before contacting the author.

### license
gpl, or something

### updates
added "notmuch.sh" and "notmuch.py". To run either first make them executable them run, as so:
```sh
% chmod 755 ./notmuch.sh ./notmuch.py
% ./notmuch.sh
% ./notmuch.py
% go build notmuch.go
% ./notmuch
```
### benchmarks
(starting with notmuch.c)
```sh
$ time ./notmuch

real	0m0.001s
user	0m0.000s
sys	0m0.000s
$ time ./notmuch.sh

real	0m0.002s
user	0m0.000s
sys	0m0.000s
$ time ./notmuch.py

real	0m0.014s
user	0m0.008s
sys	0m0.000s
$ go build notmuch.go
$ time ./notmuch

real	0m0.001s
user	0m0.000s
sys	0m0.000s
```
