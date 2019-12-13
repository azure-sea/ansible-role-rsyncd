Ansible Role: Rsync
=========


A brief description of the role goes here.

Requirements
------------
无\
None.

Role Variables
--------------
下面介绍了可用变量和默认值(可参照"defaults/main.yml"文件) \
The following describes the available variables and default values(refer to the "defaults/main.yml" file)

1. 运行Rsyncd的用户和家目录 \
  Users running Rsyncd and user home directory

默认是使用"vars/main.yml" 中的定义的变量 rsync_name (nobody) and rsync_home \
The default is to use the variable `rsync_name`(nobody) `rsync_home` defined in "vars/main.yml"

如果你想自定义的运行用户请在playbook中设置下面变量。\
If you want to customize the running user, please set the following variables in the playbook.


    rsync_name: nobody

2. Rsync 工作目录 \ 
   Rsync work directory

    rsync_dir: /data

3. 设置端口 \
   set Port

variable in "defaults/main.yml"

    rsync_port: 873

4. rsync 客户端用户账号和密码 \
   rsync clinet user and user password

variable in "defaults/main.yml"

    rsync_client_user: rsync
    rsync_client_passwd: 123456


Dependencies
------------
无依赖.\
None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: rsync, : rsync_name }


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
