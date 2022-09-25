**ReadMe file**

_Jagadeeswara Reddy Gummi Reddy. UFID: 5095-5833

Venkata Satya Sai Subhash Vadlamani. UFID : 4326-8265_


We have seperated our entire code into client.erl and server.erl. The server.erl part of the code contains the logic of accepting the number of preceding zeroes that we want in our bitcoin and listening to any coins that might be sent by the client. The client.erl part of code contains the code to create worker which spawns miners. These are responsible for generating a hashed string and checks if the generated hashed string contains the required number of trailing zeroes.

We first start the system from server with the command "erl -name@server<local Ipv4 address>". Then we start the server using following commands c(server). server:start_server. 

After this we get a prompt to enter the number of zeroes that we want our hashed string to contain. We input that number.

Now we start our client. we start the client using following commands erl -name "client@<local IPv4 address>".

To start the coin generation process we run the following command 
c(client).
client:calculate(<'server@local IPv4 address>, <Number of coins tha we want the program to generate>).

We spawn the same number of miners as the number of coins requested. But as and when we are not able to find a coin, miners are spawned.

  
![image](https://user-images.githubusercontent.com/65271041/192124900-6f4846a7-a7b0-4393-9bb1-fe04b81a701c.png)

(1)As can be seen from the above image for input 4 we have achieved CPU time as 3878, real time 1383 and the ratio as 2.80404916


![image](https://user-images.githubusercontent.com/65271041/192125868-30dcd471-5487-49be-9c3f-d74f838d16c1.png)
  
(2)Coins with maximum number of preceeding zeroes that we can find is 6.
