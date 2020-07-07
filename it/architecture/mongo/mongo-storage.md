# mongo storage

- MMAP
  Early versions' mongo, memory-consuming, do not have much method to control and optimize.
- WiredTiger
  Current use storage engine, support record level lock, much better than MMAP. 
- In-Memory 
  Only hold data in memory, If the mongo server reboot,  all data is gone. It can use as primaly db, and write operation logs to slave db,  then you can get better write performance.
