# system-design-guideline
guideline for system design 

## terms & important concepts

### distributed system

a network that stores data on more than one node (physical or virtual machines) at the sam time. since all cloud applications are distributed systems, it's essential to understand the CAP theorem when designing a cloud app so that you can choose a data management system that delivers the characteristics your application needs most. 

### CAP theorem

a distributed system can deliver only two of three desired characteristics: consistency, availability, and partition tolerance (a.k.a. CAP)

#### consistency 

all client see the same data at the same time, no matter which node they connect to. this means that if data is updated at one node, it must be instantly forwarded or replicated to all the other nodes before completing the update at the node.

#### Availability

any client can request for data even if one or more nodes are down.

#### partition tolerance

partition: a communications break within a distributed system like a lost or temporarily delayed connection between two nodes. 

partition tolerance means that the cluster must continue to work despite any number of communication breakdowns bet nodes in teh system. 

## required skills for system design interview

### requirements clarification

the purpose is to identify functional requirements and non-functional requirements.

- functional requirement: system behavior, a set of operations the system will support.

ex) the system has to count video view events. you can generalize the API based on teh this requirement. for example, you might create a method called countViewEvents(videoId), but you can generalize this further if you consider more input such as event types (e.g., "view", "like", "share") and actions (e.g., "count", "sum", "average"). this ends up a method called "processEvent(videoId, eventType, function)".

- non-functional requirements: fast, fault-tolerant, and secure. how a system is supposed to be. 

### always start with simple case when design.


- users/customers
- scale (read and write)
- performance 
- cost
