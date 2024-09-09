# Java| Group chat app 
I am tasked with creating a Client and Server application that simulates a group chat.
## Table of contents
* [Project description](#Project description)
* [Dependencies](#Dependencies)
* [How to run](#How to run)
## Project description
### Introduction:
This project is a client-server group chat created in Java with a GUI, 
Database, and Junit testing. The application allows clients to communicate
with each other in real-time through the server. Clients can send messages to 
everyone in the group, send private messages to specific clients, update their local 
list, and view the local list. The coordinator has the ability to remove clients
and check if everyone is active.
----
### Features:
The following are the key features of the application:

1. Graphical User Interface: The application has a user-friendly graphical interface that makes it easy for clients to communicate with each other.

2. Database Integration: The application uses a database to store messages, user information, and other important data.

1. Coordinator Commands: The coordinator can remove clients and check if everyone is active. e.g. **/remove** **client_name** (this ends that clients program). **/check** (checks the activity status of every member in the server and tells every user who is inactive)

1. Private Messaging: Clients can send private messages to other clients by typing **/whisper** followed by the client's name followed by the message. e.g. **/whisper client_name message**

1. List Management: Clients can update their local list and display it by pressing **update list**. They can also view the local list by typing **/requestinfo**. 

1. Junit Testing: The application has been tested using Junit to ensure its stability, functionality, and reliability.
------
### Class Diagram
![Example Image](./img/rclass.png)
------
### Challenges and Solutions:
We faced several challenges during the development of the application. 
One of the major challenges was sending messages that appear in the GUI. 
This led us to rethink our approach to how messages are sent, stored, and displayed. 
We decided to use a database for message storage and retrieval, which allowed us to 
display messages in the GUI.

Another issue we faced was allowing the server to send its own messages to clients.
This was not a problem in the CLI version of the source code, but it caused SQL errors
in the GUI version. The solution to this was to have all the messages be displayed on the server terminal instead
We plan to resolve this issue in future versions of the application.
------
### Conclusion:
The client-server group chat application is a powerful tool that enables real-time communication
between clients through the server. The application has a user-friendly GUI,
database integration, Junit testing, and features such as private messaging,
list management, and coordinator commands. We are committed to improving the application 
in future versions by resolving any outstanding issues and adding new features to enhance 
its functionality and reliability. In the future, we wish to add the ability for the coordinator to make other clients
into coordinators.
------
# Dependencies
This project uses Maven for managing dependencies. All dependencies are listed in the pom.xml file,
which can be found in the root directory of the project.

The following dependencies are required to run the application:

* __org.junit.jupiter__ version 5.7.1

If you are building the project from scratch, you will need to have these dependencies installed on your machine.
Alternatively, you can use Maven to manage the dependencies automatically. To do this, run mvn install from the root 
directory of the project, and Maven will download and install all required dependencies.

Note that if you are distributing this project to others, they will also need to have these dependencies installed on 
their machines, or they can use Maven to manage the dependencies automatically as described above.

# How to run
1. ensure that the source Directory (src) is the sources root folder. This can be done by rightclicking the ****src** Directory** 
-> **Mark Directory As** -> **Sources Root**

![Example Image](./img/sourceRoot.png)

2. Ensure you IDE and run multiple instance of the same Class. In IntellgiJ, this can be achieved by going to **Run** in
the toolbar-> **Edit configuration** -> under **Applications** Select **Client** -> under **build and run**, select **modify options** -> 
then Select **allow multiple instances** -> select **apply** then **ok**.
3. PLEASE ENSURE THAT YOU ALSO BUILD THE PROJECT BY PRESSING THE GREEN HAMMER BUTTON ON THE TASKBAR

![Example Image](./img/green.png)


3. run the **Server.main()**. This class can be found  [here](src/Main/server/Server.java).

![Example Image](./img/Serverrun.png)

You should then see the Server GUI. Note the IP Address and Server port.

![Example Image](./img/ServerGUI.png)

4. run the **Client.main()**. This class can be found  [here](src/Main/client/Client.java).

![Example Image](./img/Clientrun.png)

5. Then you should be greeted by a small "client login" screen. enter a name and then click enter.

![Example Image](./img/clientlogin.png)

6. Now you should be greeted by the "connect to server" screen. note that every client is given and unique ID that they
cannot edit. The user will have to enter the IP address and Port displayed in the Server terminal then click enter.

![Example Image](./img/Serverlogin.png)

7. Congratulations, you have connected to the server and entered the chat!

![Example Image](./img/rclient_chat.png)

8. To enter command or send messages use the Text field at the bottom of the window then click **Send**.

![Example Image](./img/rsendmessage.png)   

9. To add another client complete Step 4-7 again. Please note that whenever a new member joins then each member must
type and send **/updatelist** to update there local list otherwise they will be deemed "Inactive".

