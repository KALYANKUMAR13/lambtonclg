## install jenkins https://www.jenkins.io/doc/book/installing/linux/
sudo apt update
sudo apt install openjdk-11-jre

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

## Authentication with private repo

create keys: ssh-keygen -t ed25519 -C "foobar@example.com"