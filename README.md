# client-server-game-made-with-C
Project Objective
The objective of the project is to develop a simple client-server application that allows the client to guess a five-letter word within a certain number of attempts.

Development Environment
Virtual machine with Linux environment

Folder Contents

Server.c: contains the server code
Client.c: contains the client code
Parole.txt: contains a list of five-letter words that will be chosen by the server
Relazione_progetto_20039284.pdf: contains the project report
Program Execution
To run the program:

bash
Copia codice
gcc server.c -o server  
./server <port_number> <max_attempts>
bash
Copia codice
gcc client.c -o client  
./client <server_ip_address> <port_number>
Code Description

Server.c

Opening file containing five-letter words
Storing words in an array
Setting the number of attempts
Creating the socket
Binding the socket
Listening on the socket
Accepting the connection on the socket
Resetting the number of attempts
Setting the word to guess for this connection
Sending the welcome message
Starting the game
Closing the connection with the client
Client.c

Creating the socket
Connecting to the server
Reading the welcome message
Brief explanation of the rules
Starting the game
Closing the connection with the server
Remarks

The number of attempts is optional; if not specified during the execution, it will be set to a default of six.
The program will load 200 words from the file containing five-letter words, and one will be randomly selected when the connection with the client is initiated. This word will be the one to guess.
The client will perform a do while loop to allow the user to input a correct command (either "word" or "quit"). The server can handle any invalid commands from the client.
