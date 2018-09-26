## Hyperledger Fabric Student Record Application
## Donot forget to watch the video of this application in Video section(Please drag and drop the file on VLC media player to start with)

 This application is developed and tested on UBUNTU(16.04 LTS) as part of Blockchain Hackathon conducted by Blockchain Council.Open Source references are taken inorder to  develop this application on top of Tuna-app.
 
Requirements :
1. https://hyperledger-fabric.readthedocs.io/en/release-1.2/prereqs.html
Please follow the above link to install prerequisite such as Docker container, NPM packages etc.

2.Clone this repository to the Ubuntu system using (git clone http://....) 

3.Move to tuna-app folder.

4.Make sure you have Docker running on your machine before you run the next command.First, remove any pre-existing containers, as it may conflict with commands.
$ docker rm -f $(docker ps -aq)

5.Then, let’s start the Hyperledger Fabric network with the following command:
$ ./startFabric.sh

Troubleshooting: If, after running the above you are getting an error similar to the following:

ERROR: failed to register layer: rename
/var/lib/docker/image/overlay2/layerdb/tmp/write-set-091347846 /var/lib/docker/image/overlay2/layerdb/sha256/9d3227c1793b7494e598caafd0a5013900e17dcdf1d7bdd31d39c82be04fcf28: file exists

try running the following command:

$ rm -rf ~/Library/Containers/com.docker.docker/Data/*

6.Install the requires package, , register the Admin and User components of our network, and start the client application with the following commands:

$ npm install

$ node registerAdmin.js

$ node registerUser.js

$ node server.js

Load the client simply by opening localhost:8000 in any browser window of your choice, and you should see the user interface for our simple application at this URL as shown in the video.



