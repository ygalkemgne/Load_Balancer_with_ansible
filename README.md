Use this script to deploy 4 servers into AWS, install Haproxy in one and httpd in the 3 other servers. 
Use the vault.yaml file to store your access and secret key. Make sure the IAM user has programatic access otherwise it will not work.
Use the vault_pass_file to store you vault password after encryption. Use this command to encript your vault file. # ansible encrypt vault.yml
