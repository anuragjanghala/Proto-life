# Proto-life
# Controlled-client-Server-Client-Message-Sender

## About
Here, in this network student can record their presence in any activity inside trinity using IOT based device and mobile application, device will scan the data from mobile app of a student and then communicate with the class server and trinity server to verify that student data is right or not tampered on database and to store that presence of student inside a blockchain based database on teachers block. So here I am providing the details on how devices will communicate with each other to send, verify and store that information.Also, I am only providing the communication between students as a client using IOT device and Class server.
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
$ python ctrlP2P.py --name=classserver_1 --port=9900
```
#### for Student Client
for student 0:
```shell
$ python ctrlP2P.py --name=student0 --port=9900
```
for student 1:
```shell
$ python ctrlP2P.py --name=student1 --port=9900
```
these commands will create server and clients for the network

## Example
For server and client running on the same system for the first time

**Server classserver_1**
> $ python ctrlP2P.py --name=classserver_1 --port=9900
<pre>
Server listening to port: 9900 ...
Chat server: got connection 6 from ('127.0.0.1', 52630)
Chat server: got connection 7 from ('127.0.0.1', 52636)
</pre>

**Client student 0**
> $ python ctrlP2P.py --name=student0 --port=9900
<pre>
Now connected to chat server@ port 9900
To exit press 'ctrl+C'

To enter Private Mode type 'private/PRIVATE'and
To exit from Private mode type (-1) twice while inside private

[student0@127.0.0.1]> 
(Connected: New client (2) from student1 @ 127.0.0.1)
[student0@127.0.0.1]> 
</pre>

**client student 1**
> $ python ctrlP2P.py --name=student1 --port=9900
<pre>
Now connected to chat server@ port 9900
To exit press 'ctrl+C'

To enter Private Mode type 'private/PRIVATE'and
To exit from Private mode type (-1) twice while inside private

[student1@127.0.0.1]> 
</pre>

### working with sending connection message from a student to another student (but not to all students)
assuming that server is running and three clients is connected by using the given commands in example above

Now if you want to send message to all students to verify its presence type msg `hi to all` from student0 client
<pre>

[student0@127.0.0.1]> hi to all

</pre>

then in student1 and student2 will show the recieved message:

**in student1**
<pre>
[student1@127.0.0.1]> got message from [student0 @ 127.0.0.1]>> hi to all
</pre>
**in student2**
<pre>
[student2@127.0.0.1]> got message from [student0 @ 127.0.0.1]>> hi to all
</pre>

Now if you want to work on private mode functionality which will send message to the selected client student.

here is the example if student0 sends private message to student1: type `private` 
then in student0 client enter the client target no. type `1` for student1 

**in client student 0**
<pre>
[student0@127.0.0.1]> private
---------------Entering private mode-----------------
[student0@127.0.0.1]> 1
[student0@127.0.0.1]> hello to student1
</pre>

student1 will recieve that message but student2 wont:

**in client student 1**
<pre>
[student1@127.0.0.1]> got message from [student0 @ 127.0.0.1]>> hello to student1
</pre>

**in client student 2**
<pre>
[student2@127.0.0.1]> 
</pre>

here in the upper block we can see that student2 does not recieve any message as student0 asked for private message to student1.

In student0 client, it will stay in private mode to send another message to any other client via server untill we command to close the private mode.

**for closing private mode in student0**
<pre>
[student0@127.0.0.1]> -1
----------------------Exiting private mode----------------
[student0@127.0.0.1]> -1
</pre>

**Now for closing the each client**
> [student0@127.0.0.1]> ^C 

press ctrl+c and then press `enter`

**Now for closing server**
> [student0@127.0.0.1]> ^C 

press ctrl+c and then press `enter`

