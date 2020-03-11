# Proto-life
# Controlled-client-Server-Client-Message-Sender

## About

## Environment
It will run only on Linux and MAC
## Requirements
It will require python to be installed on your machine
```shell
$ sudo apt-get install python
```
and also download pip using:
```shell
$ pip install pip
```
Now, You can doenload python libraries using pip:

for socket:
```shell
$ pip install socket
```

for termcolor:
```shell
$ pip install termcolor
```

## Download
Run the following command in your terminal to save the repository in tour system
```shell
$ git clone https://github.com/anuragjanghala/Proto-life.git
```

## Run
Once you download the file `ctrlP2P.py`, you can create server and clients using the same file 
then run by typing the following commands in your terminal:

#### for Class Server
```shell
$ python ctrlP2P.py --name=classserver_1 --port=8800
```
#### for Student Client
for student 0:
```shell
$ python ctrlP2P.py --name=student0 --port=8800
```
for student 1:
```shell
$ python ctrlP2P.py --name=student1 --port=8800
```
these commands will create server and clients for the network

## Example
For server and client running on the same system
