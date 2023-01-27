# Practice COBOL

Practice COBOL

```bash
$ docker run --rm -itv "$(pwd):/oscobol/src" opensourcecobol/opensource-cobol

# ./HELLOWORLD: error while loading shared libraries: libcob.so.1: cannot open shared object file: No such file or directory
$$ find / -type f -name 'libcob*'
/usr/include/libcob.h
/usr/lib/libcob.a
/usr/lib/libcob.so.1.0.0
/usr/lib/libcob.la
$$ export LD_LIBRARY_PATH=/usr/lib

$$ cd /oscobol/src/
$$ cobc -x ./HELLOWORLD.cbl
$$ ./HELLOWORLD
Hello World
```


## Links

- [Neo's World](https://neos21.net/)
