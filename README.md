# c-compiler
簡単なcコンパイラです

```
docker build -t compilerbook https://www.sigbus.info/compilerbook/Dockerfile
docker run --rm -v $HOME/cc:/cc -w /cc compilerbook make test
```
