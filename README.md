https://codewithkarani.com/2023/12/31/how-to-install-erpnext-version-15-in-ubuntu-a-step-by-step-guide/?srsltid=AfmBOorgbrFIeIlcwBo7V073Ww-YdxVKYxmmkLHdnCOlB1M8terbFr_B

-----------------------------

sudo apt-get update
sudo apt-get upgrade -y

sudo adduser manal
sudo usermod -aG sudo manal
su - manal
cd /home/manal

sudo apt-get install python3
sudo apt-get install python3.10
sudo apt-get install python3-setuptools
sudo apt-get install python3-pip
sudo apt-get install python3-distutils
sudo apt-get install python3.10-venv
sudo apt update
sudo apt install python3-venv

python3 -m venv frappe-venv
sudo apt-get install software-properties-common
sudo apt install mariadb-server mariadb-client
sudo apt-get install redis-server
sudo apt-get install -y xvfb libfontconfig1 wkhtmltopdf libmysqlclient-dev

 sudo mysql_secure_installation
sudo nano /etc/mysql/my.cnf
sudo service mysql restart
sudo apt install curl
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash source ~/.profile nvm install 18
sudo apt-get install npm
sudo npm install -g yarn

source frappe-venv/bin/activate
pip install frappe-bench
bench init --frappe-branch version-15 frappe-bench

cd frappe-bench
chmod -R o+rx /home/manal
bench new-site library.localhost
bench start -> http://library.localhost:8000/
