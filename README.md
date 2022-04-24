## deploy-jenkins-server ##  

`az group create --name vmjenkins --location "east asia"`

`az vm create --resource-group vmjenkins \`  
`--name jenkinsserver \`  
`--image CentOS \`  
`--admin-username jenkins \`  
`--generate-ssh-keys \`  
`--size Standard_B1s `  
[check vm sku here](https://azureprice.net/)  

`az vm open-port --resource-group vmjenkins --name jenkinsserver --port 8080 --priority 1001`  

get the public i.p of the VM  
`ssh jenkins@<PUBLIC IP>`  
`sudo yum install java-1.8.0-openjdk-devel`  
`sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo --no-check-certificate`  
`sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key`  
`sudo yum install jenkins`  
`sudo systemctl start jenkins`  
`sudo systemctl status jenkins`  

`sudo yum install git` 

Using your browser, go to <PublicIP:8080>  
Should see the following screenshot  
Select install selected plugins  
Create first admin user  
  
Done!  