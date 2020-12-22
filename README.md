Role Name
=========
codezm.mysql

Requirements
------------

RHEL/CentOS：7、8

Role Variables
--------------

涉及变量在 `vars/main.yml` 文件中

Dependencies
------------
codezm.base

Example Playbook
----------------
##### 使用源安装方案
1. 自定义 `repo` 文件，放置于 `files` 目录中
    ```yml
    _mysql_repo_type: "file"
    _mysql_repo_file: "mysql-community-RHEL-8.repo"
    ```
2. `repo` url 地址
    ```yml
    _mysql_repo_type: "rpm"
    _mysql_package_name: "http://mirrors.ustc.edu.cn/mysql-repo/mysql80-community-release-el8-1.noarch.rpm"
    ```

##### 不使用源安装方案
1. 下载 `mysql-community-server` 软件包及其依赖包，默认使用此模式。
2. 提前将 `mysql-community-server` 相关软件包下载至 `files` 目录，并指定 `-e "env_install_way=file"` 作为执行参数。

License
-------

BSD
