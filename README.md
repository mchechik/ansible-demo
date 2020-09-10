# ansible-demo


### Command ex's
ansible-playbook -i inventory/ec2.py hardware.yml -e '{"ec2_names": ["green","blue"]}'
<br>ansible-playbook --private-key ~/.ssh/kali.pem -i inventory/ec2.py software.yml

### Ad-hoc command ex's
ansible -i inventory/ec2.py --private-key ~/.ssh/kali.pem -m shell -a 'rm -rf /home/ubuntu/server' tag_Name_Webserver*
