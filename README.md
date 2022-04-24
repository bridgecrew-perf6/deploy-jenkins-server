## deploy-jenkins-server ##  

`az group create --name vmjenkins --location "east asia"`

`az vm create --resource-group vmjenkins \`  
`--name jenkinsserver \`  
`--image CentOS \`  
`--admin-username jenkins \`  
`--generate-ssh-keys \`  
`--size Standard_B1ls `  