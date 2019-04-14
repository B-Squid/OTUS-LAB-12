`[root@bacula-server ~]# bconsole`  
Connecting to Director localhost:9101  
1000 OK: bacula-dir Version: 5.2.13 (19 February 2013)  
Enter a period to cancel a command.  
`*list jobs`  
Automatically selected Catalog: MyCatalog  
Using Catalog "MyCatalog"  
<pre>
+-------+------------+---------------------+------+-------+----------+------------+-----------+
| jobid | name       | starttime           | type | level | jobfiles | jobbytes   | jobstatus |
+-------+------------+---------------------+------+-------+----------+------------+-----------+
.
.
|    20 | Backup etc | 2019-03-27 20:06:48 | B    | F     |    2,405 | 31,058,319 | T         |
|    21 | Backup etc | 2019-03-27 20:10:02 | B    | I     |        0 |          0 | T         |
|    22 | Backup etc | 2019-03-27 20:20:02 | B    | I     |        0 |          0 | T         |
|    23 | Backup etc | 2019-03-27 20:30:02 | B    | D     |        0 |          0 | T         |
|    24 | Backup etc | 2019-03-27 20:30:05 | B    | I     |        0 |          0 | T         |
|    25 | Backup etc | 2019-03-27 20:40:02 | B    | I     |        0 |          0 | T         |
|    26 | Backup etc | 2019-03-27 20:50:02 | B    | I     |        0 |          0 | T         |
|    27 | Backup etc | 2019-03-27 21:00:02 | B    | D     |        0 |          0 | T         |
|    28 | Backup etc | 2019-03-27 21:00:05 | B    | I     |        0 |          0 | T         |
|    29 | Backup etc | 2019-03-27 21:10:02 | B    | I     |        0 |          0 | T         |
|    30 | Backup etc | 2019-03-27 21:20:02 | B    | I     |        3 |         29 | T         |
|    31 | Backup etc | 2019-03-27 21:30:02 | B    | D     |        3 |         29 | T         |
|    32 | Backup etc | 2019-03-27 21:30:05 | B    | I     |        0 |          0 | T         |
|    33 | Backup etc | 2019-03-27 21:40:02 | B    | I     |        0 |          0 | T         |
|    34 | Backup etc | 2019-03-27 21:50:02 | B    | I     |        0 |          0 | T         |
|    35 | Backup etc | 2019-03-27 22:00:02 | B    | D     |        3 |         29 | T         |
|    36 | Backup etc | 2019-03-27 22:00:05 | B    | I     |        0 |          0 | T         |
|    37 | Backup etc | 2019-03-27 22:05:02 | B    | F     |    2,407 | 31,058,348 | T         |
</pre>
END  
  
================================================================================================  
  
`*list files jobid=20`  
<pre>
+--------------------------------------------------------------------+
| filename                                                           |
+--------------------------------------------------------------------+
| /etc/                                                              |
| /etc/client-inited                                                 |
| /etc/vimrc                                                         |
| /etc/bacula/                                                       |
| /etc/bacula/examples/                                              |
| /etc/bacula/examples/bacula-fd.conf                                |
| /etc/aliases.db                                                    |
| /etc/.updated                                                      |
| /etc/hostname                                                      |
| /etc/locale.conf                                                   |
| /etc/vconsole.conf                                                 |
| /etc/sudoers.d/                                                    |
| /etc/sudoers.d/vagrant                                             |
| /etc/sudoers                                                       |
| /etc/sudo.conf                                                     |
| /etc/sudo-ldap.conf                                                |
| /etc/mke2fs.conf                                                   |
.
.
.
| /etc/selinux/targeted/                                             |
| /etc/selinux/targeted/active/                                      |
| /etc/selinux/targeted/active/policy.linked                         |
| /etc/selinux/targeted/active/users_extra.linked                    |
| /etc/selinux/targeted/active/seusers                               |
| /etc/selinux/targeted/active/seusers.linked                        |
| /etc/selinux/targeted/active/users_extra                           |
| /etc/selinux/targeted/active/policy.kern                           |
| /etc/selinux/targeted/active/homedir_template                      |
| /etc/selinux/targeted/active/file_contexts.homedirs                |
| /etc/selinux/targeted/active/file_contexts                         |
| /etc/selinux/targeted/active/commit_num                            |
| /etc/selinux/targeted/active/modules/                              |
| /etc/selinux/targeted/active/modules/disabled/                     |
| /etc/selinux/targeted/active/modules/100/                          |
| /etc/selinux/targeted/active/modules/100/zosremote/                |
| /etc/selinux/targeted/active/modules/100/zosremote/lang_ext        |
| /etc/selinux/targeted/active/modules/100/zosremote/hll             |
| /etc/selinux/targeted/active/modules/100/zosremote/cil             |
.
.
+--------------------------------------------------------------------+
+-------+------------+---------------------+------+-------+----------+------------+-----------+
| jobid | name       | starttime           | type | level | jobfiles | jobbytes   | jobstatus |
+-------+------------+---------------------+------+-------+----------+------------+-----------+
|    20 | Backup etc | 2019-03-27 20:06:48 | B    | F     |    2,405 | 31,058,319 | T         |
+-------+------------+---------------------+------+-------+----------+------------+-----------+
</pre> 

================================================================================================  
  
`*list files jobid=30`  
<pre>
+------------+
| filename   |
+------------+
| /etc/test1 |
| /etc/test2 |
| /etc/      |
+------------+
+-------+------------+---------------------+------+-------+----------+----------+-----------+
| jobid | name       | starttime           | type | level | jobfiles | jobbytes | jobstatus |
+-------+------------+---------------------+------+-------+----------+----------+-----------+
|    30 | Backup etc | 2019-03-27 21:20:02 | B    | I     |        3 |       29 | T         |
+-------+------------+---------------------+------+-------+----------+----------+-----------+
</pre> 
 
================================================================================================  
  
`*list files jobid=31`  
<pre>
+------------+
| filename   |
+------------+
| /etc/test1 |
| /etc/test2 |
| /etc/      |
+------------+
+-------+------------+---------------------+------+-------+----------+----------+-----------+
| jobid | name       | starttime           | type | level | jobfiles | jobbytes | jobstatus |
+-------+------------+---------------------+------+-------+----------+----------+-----------+
|    31 | Backup etc | 2019-03-27 21:30:02 | B    | D     |        3 |       29 | T         |
+-------+------------+---------------------+------+-------+----------+----------+-----------+
</pre>
