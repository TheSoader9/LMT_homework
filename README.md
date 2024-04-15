# LMT_homework

1. To add new user to any host or hosts, run ansible playbook command (for example):
   ansible-playbook -u root -i hosts/datacenters playbooks/newuser.yml -e "target_hosts=AAA user_name=newUser" -kK

2. To install chrony and set NTP server, run ansible playbook command (for example):
   ansible-playbook -u root -i hosts/datacenters playbooks/chrony.yml -e "target_hosts=AAA" -kK

3. To install and configure zabbix agent2, run ansible playbook command (for example):
   ansible-playbook -u root -i hosts/datacenters playbooks/zabbix-agent.yml -e "target_hosts=AAA zabbix_server_IP=YOUR-ZABBIX-SERVER-IP" -kK

   Or use parameters --user root --private-key ~/.ssh/key if you have user access key for connection.
