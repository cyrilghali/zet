# Manage multile server with Ansible

## Config your hosts

```
[group_a]
192.168.60.[1-5]

[group_b]
192.168.60.6

[group_c:children]
group_a
group_b

[group_c:vars]
ansible_ssh_port=22
```
