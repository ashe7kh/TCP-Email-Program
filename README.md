# TCP-Email-Program

Overview:

Our code functions by creating a simple yet effective TCP channel from which a client can send a message to a server who
then preserves the information. The TCP channel operates locally out of port 9000 of the machine. Rather than allow the
user to decide which port to communicate from, we believed that declaring it ourselves would prevent future issues from
arising. Two programs exist to facilitate this dialogue, one is the server who receives the message and the other being
the client who sends it. The server holds a record of all communication which has occurred through the channel.
Upon receiving an email the server responds by sending a copy of the email to the client, while simultaneously
triggering the termination protocol. The termination protocol exists the program preventing further communication. The
type of message which can be sent through this particular TCP channel is exclusively an email messages. The email
message contains a total of 5 fields which are populated by the client through the command line;
they are: the desired address (to), the name of the sender (from), the title of the message (title), the body of the
email (content), as well as the time it was sent (time).


How to execute:

1. Begin by entering "go run server.go" on your machine's command line, this program will create the server, allowing the client's
message to "exists" somewhere.
2. Secondly enter "go run client.go" in a separate command line, this program will them prompt the user to enter their email
message.
3. Enter desired email message following format outlined in prompt. The email must contain all fields specified,
separated by a semicolon ";".
4. Once the server receives an email it will respond by sending a confirmation email to the client and then close the
TCP channel. Confirmation email contains a copy of the Client's email.


Additional information:

Our process A is contained in the "ProcessA(server).go" file, and the process B is contained in "ProcessB(client).go file". We defined the "email" struct entirely within the "server.go" file, thus making the entire email struct on the serverside of the program.
