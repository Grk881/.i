#   "Thank You!"

![Screenshot 2025-01-04 105945](https://github.com/user-attachments/assets/ae327952-76bd-431e-a01e-62c419287ff8)

                                          Jenkins


-	Jenkins is an open -source
-	It is mostly use for an automation
-	Jenkins support all cloud provider  (aws-azure-gcp)
-	Jenkins is CICD pipeline tool
ex :- other cicd tools – gitlab , Jenkins , github actions , aws codepipeline ,google cloud platform , buildbot , circle ci , teamcity , bamboo , azure devops server , spinnaker

-	Jenkin is automation

•	SDLC lifecycle 
 


•	Build has  any programming lang and interpreter and compile 

•	Every code is translated into machine language through a compilation process. Each build incorporates a specific programming language, which relies on either an interpreter or a compiler. In essence, every programming language utilizes these tools—interpreters and compilers—to convert code into a format that machines can understand.

•	 any language has a compile an interpreter availability that is programming language


•	Programming  languages
  

•	Jenkins workflow  CICD pipeline


-	So , cicd pipeline is a transfer a code git to a live server 
 
•	A CI/CD pipeline involves moving code from Git to a production server , which is reffered to as CI/CD 
 
 

•	Jenkins installed laptops and servers also
 


	 Jenkins lecture 1st 

	Jenkins installation

sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install Jenkins
jenkins –version

•	add port no  8080 in security groups inbound rules 

 


•	hit public ip with  :8080

 

•	To run command for admin password 
  sudo cat /var/lib/jenkins/secrets/initialAdminPassword

ex:-       ubuntu@ip-172-31-84-62:~$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
db0002d978614b8e96201234b5d71cea


Password :-         db0002d978614b8e96201234b5d71cea
•	Enter this password to administrator password to unlock jenkins 
•	 

•	 

•	 


•	 

•	 


•	 


####     1st project     -    simple java project
•	 
•	Create folder – my folder 
•	Create subfolder -  myjavaproject 
•	Open myjavaproject folder in git bash
•	Login github 
•	Create new public repository -  myjavaproject
•	 

•	Run these commands in gitbash

 

•	 
class Test
{
    public static void main(String []args)
    {
        System.out.println("My First Java Program.");
    }
};
•	 

•	 

 

 
 

•	add git code url link in jenkins
  

 

 

•	 
 
                             


	Set up webhook git hub


 

•	In payload url *   -    http://publicip :8080/github-webhook/          
•	(jenkins url) in browser
•	 

 

 




	In jenkins

 


•	Nest step is -     changes in myjava.java file

 

•	changed file push 

 

	Changes in jenkins automate
 
 

 





  

 

	Jenkins all project stored in WORKSPACE

 

	 To check all jenkions project in terminal

 


	New task/project

	  Node js project


•	First clone github repository in git terminal 
-	  git clone https://github.com/Grk881/nodejs.git
 


•	Nano package.json
package.json


{
  "name": "my-node-app",
  "version": "1.0.0",
  "description": "A simple Node.js application",
  "main": "app.js",
  "scripts": {
    "start": "node app.js"
  },
  "author": "Your Name",
  "license": "MIT",
  "dependencies": {
    "express": "^4.18.4"
  }
}


•	nano index.js 

app.js





// Import the Express module

const express = require('express');
 
// Create an Express application

const app = express();
 
// Define a route for the root URL

app.get('/', (req, res) => {

  res.send('Hello, World!');

});
 
// Define the port number and start the server

const port = 3000;

app.listen(port, () => {

  console.log(`Server running at http://localhost:${port}/`);

});

 

 

•	 

 

•	 



	Next step 

 

-	 

-	 


-	 

-	 

-	 

-	 

-	 


-	Jenkins browser url paste in payload url section

 

 

-	 

-=-    next step 

Create app.js file 
And make changes in that file    ex :  hello world change to “hi world”

-	Git add . 
-	Git commit -m “third commit”
-	Git push origin master 

	 Automatically changes in jenkins after that 

Shows error :     


	In jenkins :    enter manage jenkins and then installed plugins install npm
	In jenkins :  enter tools n
	Select node js intallations & save


                          


	 In node build project enter configure select  and save
 
 


	After all configuration done 
 
 

 

 

 


*****      Jenkins day -  2 
	  Node js  ( test ) project

	1st step

-	    Create folder -        mkdir node 
                                       Cd node/
                                         Ls 
    Create file  -            nano package.json

-	Code :- 







{
  "name": "my-node-app",
  "version": "1.0.0",
  "description": "A simple Node.js application",
  "main": "app.js",
  "scripts": {
    "start": "node app.js"
  },
  "author": "Your Name",
  "license": "MIT",
  "dependencies": {
    "express": "^4.18.4"
  }
}

  












  Create file -             nano app.js   or vi app.js









Code :-   

// Import the Express module

const express = require('express');

// Create an Express application

const app = express();

// Define a route for the root URL

app.get('/', (req, res) => {

  res.send('Hi, World!');

});

// Define the port number and start the server

const port = 3000;

app.listen(port, () => {

  console.log(`Server running at http://localhost:${port}/`);

});

 

-	Git config in terminal

	 

	 

                                                                                                                             Git hub repository  code link https

•	Scenario -     

	Next step  =
 
	In source code m



	In source code management
 


•	In build triggers / or  triggers—
•	 

•	In build environment 
 


•	In build steps 
-	In build steps select -   execute shell 
 


•	 

	 Next step -   conduct a test on the nodetest

•	We need to make changes in the package.json and app.js files in Git first. Once these updates are made, they should automatically sync to GitHub. Following that, Jenkins should trigger an automatic release, followed by an automatic build and testing process. Lastly, it's crucial to set up a webhook in GitHub for seamless integration.

•	Scenario

 

•	




•	

•	 
 


•	Changes in app.js file   (“Hi world” changes to “Hi , folks”) 
-	 Vi app.js    
•	CODE:- 
// Import the Express module

const express = require('express');

// Create an Express application

const app = express();

// Define a route for the root URL

app.get('/', (req, res) => {

  res.send('Hi, folks');

});

// Define the port number and start the server

const port = 3000;

app.listen(port, () => {

  console.log(`Server running at http://localhost:${port}/`);

});
 

•	password for a ubuntu@ip-172-31-91-70:~/node$ git push origin master
•	Username for 'https://github.com': Grk881

-	To generate token steps 
 
•	Password for 'https://Grk881@github.com':
-	For a password settings & select developer setting in github & go to token classic 
-	Generate new token classic &  select repo section & write packages & project section 
-	Then generate token  &  paste the token id in password section

-	 

-	 


 

Output :-    We only changes in git in app.js  file 

Changes are :-   “hi world!” to “hi folks”



 
 

Console output in jenkins :- 


Started by upstream project "nodebuildproject" build number 5
originally caused by:
 Started by GitHub push by Grk881
Running as SYSTEM
Building in workspace /var/lib/jenkins/workspace/nodetest
The recommended git tool is: NONE
No credentials specified
Cloning the remote Git repository
Cloning repository https://github.com/Grk881/nodejs.git
 > git init /var/lib/jenkins/workspace/nodetest # timeout=10
Fetching upstream changes from https://github.com/Grk881/nodejs.git
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/Grk881/nodejs.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/Grk881/nodejs.git # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
 > git rev-parse refs/remotes/origin/master^{commit} # timeout=10
Checking out Revision 75c7dbdb91ca9faa42a12d52a42b3e206c1e213f (refs/remotes/origin/master)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 75c7dbdb91ca9faa42a12d52a42b3e206c1e213f # timeout=10
Commit message: "hi folks"
First time build. Skipping changelog.
[nodetest] $ /bin/sh -xe /tmp/jenkins2646604280498801886.sh
+ npm install

added 69 packages, and audited 70 packages in 3s

14 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
Finished: SUCCESS


 

	The nodebuildproject & nodetest are done and process through automation it is a continue integration

	Summary & steps of nodebuildproject & nodetest

 
	The next step involves managing the nodetest project utilizing or using mocha
-	There is two way 
-	1st way  is accessing or though server & installed mocha manually
-	2nd way is to open the package.json file and add the installed Mocha as a dependency

Steps :       
-	CODE FOR A : -     Package.json Code ( for add Mocha) To test a file
•	nano package.json

{
  "name": "my-node-app",
  "version": "1.0.0",
  "description": "A simple Node.js application",
  "main": "app.js",
  "scripts": {
    "start": "node app.js",
    "test": "mocha"
  },
  "author": "Your Name",
  "license": "MIT",
  "dependencies": {
    "express": "^4.18.4"
  },
  "devDependencies": {
    "mocha": "^10.0.0"
  }
}

Example:  
•	 

•	Create folder called test :

-	     mkdir test            
-	       cd test/
-	      nano test.js
 
 


•	Code for test.js file

var request = require('supertest');
var app = require('../app.js');

describe('GET /', function() {
  it('respond with 404 page not found', function(done) {
    request(app)
      .get('/nonexistentpage')
      .expect(404)
      .end(function(err, res) {
        if (err) {
          // If there's an error, log it and pass it to the>          console.error(err);
          return done(err);
        }
        // If everything is fine, invoke the done callback
        done();
      });
  });
});

•	Back to a previous directory 
 
•	 
•	Node modules folder create automatically so, folder location define 

 

	Next step : -    The next step is to access Jenkins, navigate to the configuration section, and under build steps, select "Execute Shell." Here, you need to add the command chmod +x ./node_modules/mocha/bin to ensure that this file is tested properly.
	Next step :-   
 
 
 
-	So basically, our nodebuild and nodetest  testing has been done
	 our third project is now in the deployment phase, and we are officially launching or deploy it on the live server.


•	So ,   We have need  the live server setups, and both the build and testing phases are ready. The node modules folder will be generated automatically. In the final phase, this folder needs to be transferred to or connected with the live server.

•	We need set up a new server or launch instance where we installed Node.js and npm, as well as established the necessary Node module connections.

	Steps :- 

•	Launch a Ubuntu instance
 

•	Scenario :- 
  

•	Live Ubuntu server  
•	Steps :--

git apt update -y
sudo apt install git
mkdir node
cd node/
git config --global user.name "Grk881"
git config --global user.email gajanankodare1997@gmail.com
git init
git remote add origin https://github.com/Grk881/nodejs.git
git pull origin master
ls
example :-
 

	Then install nodejs
 
•	sudo apt install nodejs -y
	install npm
•	sudo apt install npm -y
-	To check npm :--        npm -v
-	 
•	Command- :--         npm install
•	Command-:--     npm start
 
-	In security groups add in inbound rules 3000 port 
 

Then, 
 

	In Live server’s  ip address:3000  hit to a browser to  check response in old server 
 

•	 Hit ip adrees browser to check response  :-         54.224.205.203:3000
 

	 

-	Automate the creation of the node_modules folder on the live server as well, since Node.js and npm are required for installing npm modules in a live environment.

	Install process managers
•	sudo npm install -g pm2

	we need to start process managers 
•	pm2 start app.js

	  
-	 

	 

-	 

	For example ,   changes in live server
-	Changes  in file “hi folks” to a  “hello all”




•	nano app.js
 

 


	 to see a changes in live server 
	We have to compulsory restart   pm2


•	pm2 restart app.js
 

•	
 
•	Then changes has to be reflect
 

	Again we change app.js file 
 
-	Changes are  “Hello , All” Changed to be  “Hi , folks”
 

-	Again we have to restart  pm2
 
•	Then changes has to be reflect 
-	 

	Live server is ready
	Our live server is up and running, so we instruct Jenkins to deploy a node module to it.
 

•	Create new project in jenkins :--    nodedeploy
 
-	 
-	 
-	 
-	Navigate to a manage jenkins section in dashboard of a jenkins
-	 

-	Select     plugins 

-	Select   available plugins

-	Search      ssh 

 
 

-	In manage jenkins  section -   select  system 
 

-	 
 

-	In hostname section we have to enter :-–   live servers IP

-	In credentials section :-   select jenkins

-	In kind section -  select -  ssh username with private key 

-	 

-	In scope section :-  select – system jenkins &nodes only

-	 

-	Private key – select –   enter directly

-	 Paste live server instance   (pemkey)

 

	In jenkins nodedeploy project enter  build steps select execute shell
ssh -i N-virginia-pemkey.pem ubuntu@54.224.205.203
cd /node 
git pull https://github.com/Grk881/nodejs.git

  

 
	Steps :-  
•	 

•	 

Error as shown : -  
 

-	Not understand a pem key     
Problem:--
	(   In My case , there is only problem fault  in this project is to be a pem key , I was not paste a proper pem key in RSA formati in jenkins credentials otherwise overall all setup was perfect in *    next time for new project there servers has to be proper pem key in RSA 256 in ,  manage jenkins in system  & ssh remote hosts )
 
 

Problem in my case :  enter pem key RSA format 
 






Troubleshoot :  

-	Build now 
 
Troubleshoot :--       nodedeploy execute shell
Code :--

ssh -i git-server.pem -o StrictHostKeyChecking=no ubuntu@public key
<<--EOF
cd /node
git pull https://github.com/Grk881/nodejs.git
EOF


	In This scenario , we seen continue intyegration and continue deployment
*******  ******** ****** ****** ****** ****** ****** ***** ****** ****** ****** ***** 

	

 





