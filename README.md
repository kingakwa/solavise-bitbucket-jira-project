# solavise-bitbucket-jira-project

-create an instance
-install ansible
-sudo apt update 
-sudo apt upgrade -y
-sudo apt install -y ansible
-ansible --version

-sudo apt install -y docker.io
-sudo systemctl start docker
-sudo systemctl enable docker
-docker --version
-sudo usermod -aG docker $USER
-newgrp docker

-sudo systemctl start docker
-sudo systemctl enable docker
-sudo systemctl status docker

#install docker compose
`sudo rm /usr/local/bin/docker-compose`
`sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
1sudo chmod +x /usr/local/bin/docker-compose1
-docker-compose --version
- mkdir bitbucket
-cd bitbucket
-create inventory. ini
-vim inventory.ini
- enter this code
  
` [jira]
`localhost ansible_connection=local`

` [bitbucket]
`localhost ansible_connection=local`

- vim deploy-bitbucket.yal   -paste your code but i have already added the  code to the file

- vim deploy-jira.yaml -paste your code i have already added the code just run below code to the file.

- after run this code

  `inventory.ini deploy-jira.yml`
`ansible-playbook -i inventory.ini deploy-bitbucket.yml`

- Then create your docker-compose.yml file. i have already created the file 
- run this command 
- docker-compose up -d
- check your browser with your ip:address.


