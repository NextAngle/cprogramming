# C programming
**This repository is mainted so that we can learn c programming by writing and running code in our local machine using docker environment.**

## Clone the repository
```
git clone https://github.com/NextAngle/cprogramming.git
```

## Build the environment
Go inside project root directory and run below commands for building and running inside a docker container.
```docker
# build docker image from project root directory
docker build -t c-programming-environment .
```

## Access GCC running container and attach volume
Using below command we are running our c-programming-environment image in a container i.e. pointing to our project directory along with existing code folder
```docker
# Run docker in your current directory
docker run -it --rm -v "$(pwd)/code":/app c-programming-environment
```
After successfully running above command, you will be accessing the docker c-programming-enviroment. Now, all below command needs to run on this server.

```accessing
# you will see something like this after accessing c-programming-environment
root@f82456676901:/app#
```

## Compile c-programming code using gcc

```bash
# Compile code using gcc inside your c-programming-environment container
gcc -o main main.c
```

## Run compiled code

```bash
# Execute compile code
./main
```