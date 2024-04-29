# Step 1 - IPAM
This is where we deploy containers running phpipam.

# Software
- Docker
- Terraform

# HOWTO
Deploy:
```
terraform init
terraform plan
terraform apply
```  
After deploying, log in to phpipam using the URL as output by terraform and using the credentials mentioned below.  
In there, enable API calls under Administration -> phpIPAM settings. Scroll down to Feature settings and enable API. Hit Save down at the bottom.  
Next, go to Administration -> API to create an API key. Enter a name for the App ID (this will become part of the url: phpipam/api/<appid>/). Set the app permissions to Read / Write / Admin and verify the App security is SSL with App token. Copy the App id and App id to the file credentials.yaml in folder 02.Setup. Don't forget to hit the green Add button.  
Undo:
`terraform destroy`

# phpipam
Username: Admin  
Password: ipamadmin  
If the above don't work, look here: https://phpipam.net/demo/