![Docker Build Status](https://img.shields.io/docker/automated/smezger/svn-server-ubuntu.svg?style=plastic) ![Docker Build Status](https://img.shields.io/docker/build/smezger/svn-server-ubuntu.svg?style=plastic)
# Docker Image Source Files for smezger/svn-server-ubuntu


# Description
The Docker Image is based on **Ubuntu** with an Apache2 web-server and svn. The if.svnadmin web-interface is used to administrate svn. In addition to http:// the svn:// protocol can be used.

# Create a container from the image
To create a container with the repository data located on the host machine e.g. in the directory /data/docker/svn-server execute the following command:
```
docker run -d --name svn-server -p 80:80 -p 3960:3960 -v /data/docker/svn-server:/home/svn --restart unless-stopped smezger/svn-server-ubuntu
```
Test if everything is up and running by opening a browser and open the url 'http://localhost/svn'. As you have not specified a user yet just ignore the username and password dialog.

# Configuration
To create repositories and add users go to 'http://localhost/svnadmin/'. On the first start a username and password for the web admin interface has to be defined. 
