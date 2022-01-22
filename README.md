# ProjectZ
Project Z is going to be a secure distributed CNC/C2 server for controlling a raspberry PI Cluster. The main objective is to have the club ship features/tools for a raspberry pi cluster that Dr. Islam has provided for us. This platform will be used for us to test custom made malware, test web security, unit/load test web endpoints, perform SQL injections and much more. The possibilties are endless.


## General Features

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


## Data Repository
The data repository is responsible for accessing any databases that our tool needs. Most likely we'll be using something simple like "sqlite3" to store and data our tool needs.The data repository will also allow caching services like redis or rabbitMQ


## Services
Services are the general features mentioned above. The unix terminal, process manager and flooding engine will all be converted to code/libraries that function independently from the data repo and controllers.


## Controllers
The controllers are remote endpoints that the software needs to communicate with the cluster or the master. These could either be socket connections or HTTP endpoints.


## Models
The models service is for all the data models needed for our tool. ER-Diagrams/UML would go in this section/folder.


