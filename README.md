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
***Server classserver_1***
> $ python ctrlP2P.py --name=classserver_1 --port=8800
<pre>
Server listening to port: 9900 ...
Chat server: got connection 6 from ('127.0.0.1', 52630)
Chat server: got connection 7 from ('127.0.0.1', 52636)
<pre>

***Client student 0***
> $ python ctrlP2P.py --name=student0 --port=8800
<pre>
Now connected to chat server@ port 9900
To exit press 'ctrl+C'

To enter Private Mode type 'private/PRIVATE'and
To exit from Private mode type (-1) twice while inside private

[student0@127.0.0.1]> 
(Connected: New client (2) from student1 @ 127.0.0.1)
[student0@127.0.0.1]> 
</pre>

***client student 1***
> $ python ctrlP2P.py --name=student1 --port=8800
<pre>
Now connected to chat server@ port 9900
To exit press 'ctrl+C'

To enter Private Mode type 'private/PRIVATE'and
To exit from Private mode type (-1) twice while inside private

[student1@127.0.0.1]> 
</pre>
