# C programming
**This repository is mainted so that we can learn c programming by writing and running code in our local machine using docker environment.**

## Clone the repository
```
git clone https://github.com/NextAngle/cprogramming.git
```

## Build and run
Go inside project root directory and run below commands for building and running inside a docker container.
```docker
# build docker image from project root directory
docker build -t c-programming-environment .
```

```docker
# Run docker in your current directory
docker run -it --rm -v "$(pwd)":/app c-programming-environment
```

## compile c-programming code using gcc

```bash
# Compile code using gcc inside your c-programming-environment container
gcc -o main main.c
```

## Run compiled programming

```bash
# Execute compile code
./main
```