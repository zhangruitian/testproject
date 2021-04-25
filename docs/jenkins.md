
# Jenkins  

## install jenkins
```
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
```

## install the Open Java Development Kit (OpenJDK)
```
sudo apt update  // Update the repositories
sudo apt search openjdk  // search of all available packages
sudo apt install openjdk-11-jdk  // Pick one option and install it
sudo apt install openjdk-11-jdk  // Confirm installation
java -version  // checking installation
```

## start
```
cd /usr/share/jenkins
pm2 start 'java -jar jenkins.war --httpPort=9090' --name jenkins
```

## global config  

1. visit localhost:9090 and set a user
    * admin's password is in initialAdminPassword file (/root/.jenkins/...)
2. install recommanded plugins
3. set global configuration in system manegement
    * jenkins server URL, such as port
    * github server (you need a github access token firstly). 
        config username, github server URL that is https://api.github.com and add a auth way such as github access token
        click the test button.
        defulat hook URL is localhost:port/github-webhook/

## create a freestyle project
    * project URL in github
    * project code URL, using .git URL will be better
    * username and password in github
    * 
    * Coming soon...
    * 