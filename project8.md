## Project workflow

Step 1 - Create a project directory using git bash and cd into it. 

Step 2 - Set up a VM in the directory using VM link from vagrant cloud.

Step 3 - Edit the vagrant file to uncomment and update the IP address

![IMG-9367](https://user-images.githubusercontent.com/93732510/158658977-3284c1f4-843b-4446-a91a-4e7f55e6f503.jpg)

Step 4 - Bring up the VM and ssh into it.

![unnamed](https://user-images.githubusercontent.com/93732510/158657334-e9c6d5cb-7855-46cf-acdc-5c36e388793c.jpg)

Step 5 - Open docker installation document to see intstallation steps for linux 

Step 6 - After docker installation, give permission to user by adding it to docker group, then logout and login to the vm again to activate the change.

![IMG-9370](https://user-images.githubusercontent.com/93732510/158660239-f262a818-1ad4-439e-bd4b-1fe3f944cad1.jpg)

Step 7 - Run docker commands to check if user permission took effect.

Step 8 - Open up VS code or intellij to write docker files for the docker images.

Step 9 - Open docker hub to create 3 respositories for the docker images that needs customization (apache, nginx, mysql)

![IMG-9371](https://user-images.githubusercontent.com/93732510/158661679-a56f6e0b-df6b-431e-a348-65328d10f36b.jpg)

Step 10 - Get the tag for apache tomcat base image from docker hub and write the dockerfile in the text editor

![IMG-9376](https://user-images.githubusercontent.com/93732510/158662019-b53e325e-4b8e-4803-ad72-ccb54560e3dc.jpg)

Step 11 - Get the base image for mysql from docker hub and write its dockerfile.

![IMG-9377](https://user-images.githubusercontent.com/93732510/158662450-7b5d0a00-8a13-4ed7-afa0-f653a78871e1.jpg)

Step 12 - Get the base image for nginx and write its docker file.

![IMG-9380](https://user-images.githubusercontent.com/93732510/158662808-4c49325d-8e50-4df7-b1e2-62df4acf8f94.jpg)

Step 13 - Copy db backup.sql file into the db dockerfile.

Step 14 - Open up git bash and go in the directory inside the VM where you have the docker files

Step 15 - Install maven and jdk8 as its dependency.

Step 16 - Run mvn install command to generate the artifacts

![IMG-9383](https://user-images.githubusercontent.com/93732510/158664503-d3348522-3152-4436-b200-e0b08ac4b61f.jpg)

Step 17 - Copy the artifact in the target directory to the docker file directory

![IMG-9385](https://user-images.githubusercontent.com/93732510/158664967-7c13238e-5189-4936-8cdc-bf4ed1db53db.jpg)

Step 18 - Go in each dockerfile for mysql, tomcat, nginx and run the docker build for each.

![IMG-9386](https://user-images.githubusercontent.com/93732510/158668057-2b67832e-5659-4fd1-b6f9-b3fe3a42672e.jpg)

Step - 19 Get the docker base image for rabbitmq and memcachedd from docker hub.

Command: docker pull rabbitmq and Docker pull memcached.

Step 20 - Run docker images command to check for all the images.

![IMG-9388](https://user-images.githubusercontent.com/93732510/158668655-0bad9edf-be39-41bf-a580-f6f373620396.jpg)

Step 21 - Install docker compose from following installation document to test the containers.

Step 22 - Give permission to the user to run docker compose command.

![IMG-9390](https://user-images.githubusercontent.com/93732510/158672056-98ff1f0b-466d-4e5e-80c5-bc710e31748a.jpg)

Step 24 - Write a docker compose YAML file in a chosen text editor to run our containers following the documentation.

Step 25 - Open up git bash and go in the compose directory with the YAML file and run it.

![IMG-9392](https://user-images.githubusercontent.com/93732510/158674407-15f570f7-ec55-4929-ae53-5f6d950e5df3.jpg)

Step 26 - Copy the IP address from vagrantfile and check via browser to see the application is running.

![IMG-9393](https://user-images.githubusercontent.com/93732510/158674834-1a5003dd-9337-44a4-8d9d-8926193bd2a8.jpg)

Step 27 - Now to push the images in our docker hub repository, run docker login command to get in docker hub account. 

Step 28 - Run docker push and image name. 

![IMG-9395](https://user-images.githubusercontent.com/93732510/158675511-8ef45b0f-184c-461f-a0d4-51810ee9ad3f.jpg)

Step 29 - Checkthat the images have been pushed successfully.

![IMG-9396](https://user-images.githubusercontent.com/93732510/158675658-50e3b8fe-c0b9-4d9d-9304-6ca61ae40095.jpg)








