# Mysql-Setup

# Use below commands to setup Mysql Database
    wget https://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm
    yum localinstall mysql57-community-release-el7-11.noarch.rpm -y
    yum install mysql-community-server -y
    systemctl start mysqld.service
  # Here we get pwd
    cat /var/log/mysqld.log
  ![image](https://user-images.githubusercontent.com/58024415/104094459-07e6ef80-52b7-11eb-84b6-5263c15b4faf.png)
# Mysql Login command
    mysql -u root -p
# Change password for root user
    ALTER USER 'root'@'localhost' IDENTIFIED BY 'Archu@13';
# Create user with in mysql database
    create user 'loga'@'localhost' IDENTIFIED BY 'Archu@13';
    GRANT ALL PRIVILEGES ON *.* TO 'loga'@'localhost' WITH GRANT OPTION;

#Checking list of users

select host, user from mysql.user;
