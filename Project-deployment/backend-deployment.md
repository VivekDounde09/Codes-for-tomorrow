# Buy a Ubuntu Server from digital ocean or any server providers

##Install Nginx 
```
sudo apt install nginx
```
##Install nodejs
```
sudo apt install nodejs
```

##install Docker on ubuntu machine
```
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
##Install Docker's latest version
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
###Test docker is running or not
```
sudo docker run hello-world
```
##Clone repositries to container
```
git clone <URL of the Repo>
```

Server config in:
```
cd /etc/nginix/ sites-available
```
```
sudo nano <telegram-bot>
```
config ip-port and url in <telegram-bot>
```
cd /etc/nginix/ sites-enabled
sudo nano ln -s ../sites-available/api.telegram-bot.com ./
```
install mvn to change the -version of nodejs
