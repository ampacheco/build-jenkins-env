# :computer: Create Resourse Group

```
az group create -n jenkins-rg -l eastus
```

# :computer: Create Ubuntu VM
```
az vm create --resource-group jenkins-rg --name jenkins-vm --image UbuntuLTS --admin-username azureuser --generate-ssh-keys
```

# :computer: Install Jenkins
```
sudo apt update
wget -q -O - http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt update
sudo apt install jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```

# :computer: Publish 8080 Port
```
az vm open-port -g jenkins-rg --name jenkins-vm --port 80
```


# :computer: Get admin password
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

# :computer: Create First User
```
```

# Creaata Azure DNS some

# Udate Domain Delegation
