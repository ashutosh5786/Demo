# Demo application of httpbin

### Deployment of the Cluster
I have deployed the eks cluster with the filename *cluster.yaml* It have all the details about the cluster although its not to big.

### Jenkins
It's been running over a separate instance <br /><br />
![image](https://user-images.githubusercontent.com/56734473/138062236-5ed2dd19-5c78-4b52-9d79-fb0be4d2c9c9.png)
<br /><br />

After configuring the pipeline with the Jenkinsfile
<br /> <br /> 
![image](https://user-images.githubusercontent.com/56734473/138063233-a1896d01-ccc1-43ca-8057-fa00f1189b4c.png)
<br /> <br /> 
#### The jenkins file is downloading the code from SCM notified using the GitHubPollSCM (webhooks)
Achieving the task to run the pipeline as soon as the dev create any event in SCM.
After downloading the code it will contarized the code and push it to the dockerhub, And from then

We could use our *kubectl* commands to deploy the 
<br /> <br /> 
![image](https://user-images.githubusercontent.com/56734473/138064178-003f87c2-b29b-4b53-af62-3ad5a024b735.png)

### Service
The LoadBalancer is used as to interact with the GUI, The service yaml file present in the repo for reference <br /> <br /> 
![image](https://user-images.githubusercontent.com/56734473/138064351-2c1150a5-a3aa-44a7-bb0b-059c671fea7c.png)
<br /> <br /> 

After aceessing the ELB or LoadBalancer we can reach the endpoint for our application. <br /> <br />
![image](https://user-images.githubusercontent.com/56734473/138064501-bc03948a-bd50-455a-aa01-b31b61134840.png)

For Reference Here is the Loadbalancer from AWS Console
![image](https://user-images.githubusercontent.com/56734473/138064715-4d98eb69-c843-4fde-a159-f98a8a5d5c39.png)


## For the Pipeline I have used the pipeline present in the SCM
Due to above reason I have forked the repo and putted the Jenkinsfile over there too. click [here](https://github.com/ashutosh5786/httpbin)

More Screen Shots 
![image](https://user-images.githubusercontent.com/56734473/138065538-e9496fbf-ad3a-484c-8fe0-47423f3c602d.png)
![image](https://user-images.githubusercontent.com/56734473/138065589-c0490e8d-0af8-4a6b-950c-f055a5846cc2.png)


And that pretty much everything that was mentioned in the assignment I think 😅😅


