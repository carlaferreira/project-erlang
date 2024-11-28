# project-erlang
# CPLT - Actor-based Concurrency Module

## Erlang Lab Class #3 - Project

----
To submit your answers, simply push your files onto the repository. The problem will be graded.

----

## Mini Version Control System

In this project the goal is to implement a very simplified version control system (VCS).
There are some assumptions:
* All repositories are flat - no nested directories. 
* It considers only the server side interactions.
* Because there are no branches, the versions of a file can be represented as a sequence
If you know git commands, don't be shocked, this project commands are restricted or adapted.

### MiniVSC: Overview

* **register**
  * Users can register in the system with a given username.
  * Only registered users can use the system.
* **new**
  * Creates a new repository. It should include the username and the repo name. It defines the repo admin. 
* **invite**
  * Adds a collaborator to the repo. It should include the admin, the repo name, and the new collaborator username.
* **subscribe**
  * Notify collaborators that have subscibed for notifications of repository changes (e.g., a new file added)
* **token**
  * Allow admins to generate temporary access tokens for specific users or use cases. Tokens grant access to a repository for a limited time and after expiration, the token is invalidated.
  
The following commands are only allowed to the admin or invited collaborators of a repo:

* **add** 
  * Adds a file to the repo. It receives the username, the repo name, and the file name. This is consider to be the first version of the file.
* **push** 
  * Push a list of updated files to be repo. It receives the username, the repo name, and a list with the file names. It increases the versions of all the files pushed.
* **status** 
  * Prints the main information for repo, namely, the usernames of the admin and collaborators. For each file it should show, the last version of each file and the collaborator who made the last update. 
  
 ### MiniVSC: Structure 
The system has two components: 
* The client that sends the requests to the server; and 
* The server that manages the client's requests.
* The server can include multiple processes.

## Requirements

* Based on the projected description define the interaction protocol between client and server.
* In the project report explain your solution and what properties your implementation ensures, justifying your claims.
  * Consider what would happen if a client does not follow the agreed protocol when interacting wuth the server.


