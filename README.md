# ProjectZ
Project Z is going to be a secure distributed CNC/C2 server for controlling a raspberry PI Cluster. The main objective is to have the club ship features/tools for a raspberry pi cluster that Dr. Islam has provided for us. This platform will be used for us to test custom made malware, test web security, unit/load test web endpoints, perform SQL injections and much more. The possibilties are endless.


# General Features

1. **Distributed unix terminal**
    * Aggregate terminal results from multiple PI's
    * Accept/Recognize multiple unix terminal commands
    * Research linux commands to expand this feature
2. **Distributed Process Manager**
    * Keep track of all running PID's
    * Aggregate results of all the processes running on the PI's
    * Start/Stop/List running processes from the cluster
3. **DDOS/FLOODING ENGINE**
    * Create socket connections and be able to send data to host(target)
    * Be able to measure how many GB's our flooder is hitting
    * Make all entites in the cluster send flood attacks
    * Select which entities send the flood attack


# Data Repository
The data repository is responsible for accessing any databases that our tool needs. Most likely we'll be using something simple like "sqlite3" to store and data our tool needs.The data repository will also allow caching services like redis or rabbitMQ


# Services
Services are the general features mentioned above. The unix terminal, process manager and flooding engine will all be converted to code/libraries that function independently from the data repo and controllers.

1. **DDOS FLOODING SERVICE**
   * Will be able to perform multiple attacks at the same time
   * Distribute flood load accross the raspberry pi cluster
   * Select which raspberry pi's are involved in the attack
   * Implement a map reduce to gather results across all devices
   * Implement the following types of attacks: slowloris, TCP/UDP


2. **DISTRIBUTED LINUX TERMINAL**
   * Use the unix terminal of all PI's in the cluster
   * Be able to individually access a PI terminal in the cluster
   * Send a command to all PI's in the cluster using unix terminal
   * Figure out ways to gather terminal results and map reduce results from all devices
   
3. **DISTRIBUTED PROCESS MANAGER**
   * View pids (Process IDS) across all raspberry pi's
   * Monitor active/new processes
   * Measure delta of new processes that are started 


# Controllers
The controllers are remote endpoints that the software needs to communicate with the cluster or the master. These could either be socket connections or HTTP endpoints.

1. Create crud for all models
2.    * Create
3.    * Read
4.    * DetailView
5.    * Update
6.    * Delete
7.    * Create Many

2. Create endpoints specific to each function of the service. 

3. 

# Models
The models service is for all the data models needed for our tool. ER-Diagrams/UML would go in this section/folder.


1. Assign members for this
   * work with current reminders down below

## Device
Data model for storing device information from other raspberry pi's in the cluster. 

| FieldName        | Summary                                             |
|------------------|-----------------------------------------------------|
| Name             | Os Username of the raspberry PI/Linux Device        |
| IP Address       | Remote/Local IPv4 or public address of the device   |
| Mac Address      | Mac Address of the Device                           |
| Operating System | Current Operating system of the device              |
| Alias            | This can be some type of Alias to Identify a device |
| Shell Session    | Tells us whether web shell session is active or not |

## Attack
Data model for storing active/dormant attacks in the database. 
| FieldName    | Summary                                            |
|--------------|----------------------------------------------------|
| ID           | Unique ID to differ from other attack vectors      |
| Duration     | Duration of how long the flooding task will take   |
| Date Created | Date that the attack started                       |
| Type         | Type of flooding attack                            |
| Port         | Port that the flooding attack is taking place on.  |

## User
Data model for storing users that can access the cluster. 
| FieldName        | Summary                                                   |
|------------------|-----------------------------------------------------------|
| ID               | Unique ID to differ from other users                      |
| Username         | Username for user account                                 |
| Password         | Password: Hash with some crypto algo                      |
| Permission Group | Permission group of the user                              |
| Cookie           | Cookie that stores information like (IP, session browser) |




