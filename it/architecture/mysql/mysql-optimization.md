# mysql optimication

##  mysql server optimication
1. storage engine: InnoDB rather than MyISAM and every table has an InnoDB file
2. cache pool, ensure common query in memory.``innodb_buffer_pool_size`` choose proper value, and you can execute some query in advance when you reboot you server. Disable swap.
3. Reduce write to disk operations
   3.1) `innodb_log_file_size`, increate write cache pool size
   3.2 `innodb_flush_log_at_trx_commit`, in some case, there is no need to write to disk at once.
4. Avoid [[mysql doublewrite buffer]]
5. Increase disk read write speed. Flash disk instand of machinic mechanical hard disk, use [[soft RAID0]]
6. 
## code optimication


https://zhuanlan.zhihu.com/p/39038788