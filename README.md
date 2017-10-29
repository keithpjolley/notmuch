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
% julia ./notmuch.jl
```

### benchmarks
These were run on a micro EC2 instance and are for demonstration purposes only. Your mileage may vary. The only benchmarks that matter are your benchmarks. 
```sh
$ cc -O3 -Wall notmuch.c -o notmuch
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
$ rm notmuch
$ go build notmuch.go
$ time ./notmuch

real	0m0.001s
user	0m0.000s
sys	0m0.000s
```

This benchmark run on a mac mini
```sh
$ time /Local/Applications/Julia-0.6.app/Contents/Resources/julia/bin/julia /tmp/notmuch.jl 

real	0m0.482s
user	0m0.329s
sys	0m0.132s
```

Clearly, if you are going to run "notmuch" in production the macos/julia combo is to be avoided.
