# System Design Interview Cheat Sheet

1.	Who are the customers?
2.	Module of the system being focused?
3.	Scale of the system? Global or any geo location particularly?
4.	CAP theorem – Consistency / Availability? Based on that DB can be chosen
5.	Sequence of events in the application 
6.	Any APIs? 
7.	Microservices – for which service fulfills which API? How communication is going to happen (server to client etc? Polling or pushing?
8.	What data is needed?  Data flow and show in diagram
9.	Kind of data store? SQL/ NoSQL , capacity estimation, optimizing for read or write
10.	Scaling of DB  - vertical or horizontal ?
11.	Caching and sharding – separate DB for different country etc; which unique ID you would use for sharding?
12.	Failure and resiliency – Master/Slave architecture
13.	Health Checks / heartbeats – make sure all are monitored
14.	Logging /Monitoring
15.	Security 
16.	Algos and DS – sometimes its good to mention if any algorithms can be used
********************************************************************

# NoSQL databases 

- Write optimized
- No ACID properties
- Easy to add denormalized data / No new column to be added for new stuff to be added (JSON object)

# RAID (Redundant Array of Independent Disks)
- putting together multiple disks which act like single disk
- Different levels
     - RAID 0 (Striping) : splits data evenly across 2 or more disks giving high performance, but NO protection
     - RAID 1 (Mirroring) : gives an exact copy of data on both disks, offering great reliability 
     - RAID 4 & 5         : Same as RAID 0, but they save parity information for data saved to them. Parity data is not full data info, but helps great in recreating the data in case of failure
     - RAID 1 PLUS 0 (RAID 10) : Striped pair of mirrored disks!
- You can purchase a RAID enclosure fill with your own HDDs (hard disk drives) or SSDs(solid state drives) or preconfigured ones!

# Distributed Cache
- 2 types : Write through / Write Back
