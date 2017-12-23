# 文档地址 http://www.ansible.com.cn/docs

##`Install In Mac`

brew install Ansible

## `Add ssh_key to node`

###添加本地 public SSH key 到 authorized_keys

* ssh-keygen -t [rsa|dsa]，将会生成密钥文件和私钥文件 id_rsa,id_rsa.pub或id_dsa,id_dsa.pub
* 将 .pub 文件复制到B机器的 .ssh 目录， 并 cat id_dsa.pub >> ~/.ssh/authorized_keys

### 编辑(或创建)/etc/ansible/hosts 并在其中加入一个或多个远程系统

mail.example.com

[webservers]
foo.example.com
bar.example.com

### 测试通信是否正常

*ansible all -m ping -u ubuntu(登录名称) --become-user root
*ansible all -a "/bin/echo hello" -u ubuntu --become-user root

### 配置ansible

编辑 /etc/ansible/ansible.cfg or ~/.ansible.cfg

### Playbooks

###Variables

###Role