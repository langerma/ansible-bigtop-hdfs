# ansible-bigtop-hdfs

zookeeper must be in place and running --> see my zookeeper role

## example inventory
```ìni
[master]
master1
master2
masterq

[hdfs_namenodes]
master1
master2

[data]
data1
data2
data3
data4
data5
data6

[all:children]
master
data
```

## example playbook
```yml
- hosts: all
  remote_user: vagrant
  become: true

  roles:
    - role: ansible-bigtop-hdfs
```
