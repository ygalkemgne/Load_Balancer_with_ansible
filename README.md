Use this script to deploy 4 servers into AWS, install Haproxy in one and httpd in the 3 other servers. 
Use the vault.yaml file to store your access and secret key. Make sure the IAM user has programatic access otherwise it will not work.
Use the vault_pass_file to store you vault password after encryption. Use this command to encript your vault file. # ansible encrypt vault.yml
Create a hosts directory and move ec2.ini and ec2.py. ec2.py is used here for dynamic inventory. ansible.cfg checks is configured to check into the hosts file.
Install boto and boto3. these are requirements of ansible, also install ansible galaxy.
Run this command to change the permission of the private key chmod 400 xxxxxx.pem.
cd hosts/ and run this command chmod +x *. ec2.ini and ec2.py are files that need to be executable
Run this first playboook to get all setup ansible-playbook setup.yml --vault-password-file=vault_pass_file
Run this playbook to install haproxy and httpd. ansible-playbook pla ybook.yml
enjoy!!!!!!
