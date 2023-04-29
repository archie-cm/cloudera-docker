# cloudera-docker
Setting up a single node Cloudera Hadoop on cloud with quickstart image, docker and docker compose


### Getting Things Ready
First, it is necessary to have Docker and Docker compose running on your OS.
 

#### Setting up Single Node Cloudera Hadoop with Docker Compose  
* Get the docker-compose.yaml file from https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/cloudera-quickstart/docker-compose.yaml and store it in a proper folder  
* Change directory to the folder where docker-compose.yaml exists  
* Execute following command and wait for docker and docker compose do the things for you (If you dont want to see the trace simply execute the command on detach mode)  
``` docker-compose up ``` 
* In the end, you see following final lines that means your Single Node Cloudera Hadoop is ready to use  
![alt text](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/installation_done.png "Installation Done!")  
* Try to each and use Hue, http://IP:8888. User name and password is cloudera/cloudera  
![alt text](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/hue_login.png "Hue Login")  
![alt text](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/hue_my_documents.png "Hue My Documents")  

#### Start up Cloudera Manager
Having installation completed, Cloudera Manager is still disabled and it is better to enable it. Here is the simple guide for enabling Cloudera Manager  

* List the quickstart container and attach to it  
``` docker ps ```   
``` docker attach container-id ```  
* Execute following command in container for enabling Cloudera Manager. It will take couple of minutes to be completed  
``` /home/cloudera/cloudera-manager --express ```  
![alt text](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/cm_installed.png "CM Installed")  
* When CM is being started, it stops all services. Hence it is necessary to restart them all over Cloudera Manager
![alt text](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/cm_start.png "CM Installed")  

and We're done! Single node Cloudera Hadoop is ready for use

![alt text](https://github.com/emirkorkmaz/cloudera-quickstart-docker-compose/blob/master/misc/images/cm_services_started.png "We're Done")  
