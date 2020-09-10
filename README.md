# ansible-demo


### Command ex's
Deploy ec2's: ansible-playbook -i inventory/ec2.py hardware.yml -e '{"ec2_names": ["green","blue"]}'
<br>
Install software: ansible-playbook --private-key ~/.ssh/kali.pem -i inventory/ec2.py software.yml
<br>
Blue-green deployment: ansible-playbook -i inventory/ec2.py --private-key ~/.ssh/kali.pem software.yml --tags bg
<br>
### Ad-hoc command ex's
ansible -i inventory/ec2.py --private-key ~/.ssh/kali.pem -m shell -a 'rm -rf /home/ubuntu/server' tag_Name_Webserver*
