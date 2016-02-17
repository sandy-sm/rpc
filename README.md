# rpc
Java RMI Application 

Prerequisites:
1) Jdk v5 and above
2) rmic client
3) rmiregistry 

Step 1) Download/Clone project:

> git clone https://github.com/sandy-sm/rpc.git


Step 2) Goto rpc/ folder, Compile java files


> cd rpc/

> javac com/sandeep/RPCDemo/*.java


Step 3) Register skeleton

> rmic com.sandeep.RMIDemo.LoginInterfaceImpl


Step 4) Start rmiregistry on port 5959.

> rmiregistry 5959


Step 5) Open another command prompt, Start RMI Server with credentials file path

> java -Dcredentials.path=/home/sandeep/Desktop/RMI/com/sandeep/RMIDemo/credentials com.sandeep.RMIDemo.RmiServer

where, -Dcredentials.path=<path_to_credentials_file>
Format of file,

<username>/<password>


Step 6) Open one another command prompt for client, Start Client:

> java com.sandeep.RMIDemo.RmiClient


Step 7) Start using Remote method invocation!

----------------------------------------------------------
Sample output on RmiClient:

Application


Operations:
1. Login
2. Register as new user
exit: Exit
1
Username: 
admin
Password: 
bits123

Welcome admin!

List of users registerd: 
admin


Operations:
1. Login
2. Register as new user
exit: Exit
2
Enter username
sandeep
Enter password:
sandeep123
Registration Successfull


