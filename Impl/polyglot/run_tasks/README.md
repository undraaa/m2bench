# M2Bench: A Benchmark for Analytics in Multi-Model Databases 

## The detailed explanation file

See `m2bench.md`.

## Install

### Prerequsite

- Install cmake >= 3.11.x 
- Install neo4j client using following github
```
$ sudo apt-get install -y libedit-dev
$ sudo apt-get install cypher-lint libcypher-parser-dev
$ git clone https://github.com/majensen/libneo4j-client.git
$ cd libneo4j-client
$ sudo apt-get install libssl-dev
$ sudo apt-get install autoconf
$ sudo apt-get install libtool
$ sudo apt-get install pkg-config
$ ./autogen.sh
$ ./configure --without-tls --disable-tools
$ make clean check  # Remove  "-Wno-error=stringop-truncation -Wno-unknown-warning-option [-Werror]" in the "configure.ac" file,  if  it invokes an error. 
$ sudo make install
```

- Install mysql connector
```
download apt repository : https://dev.mysql.com/downloads/repo/apt/
$ sudo dpkg -i ....deb
$ sudo apt update
$ sudo apt install libmysqlcppconn-dev
```

- Install mongocxx connector

```
http://mongocxx.org/mongocxx-v3/installation/
```


### Build M2Bench

```
mkdir build
cd build
cmake ..
make
./m2bench
```