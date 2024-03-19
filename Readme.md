What is devOps?
ans)

What is SDLC?
ans)

What is Vm and Hypervisor.?
ans) vm is nothing but just a breaking down physical server into many parts logically using or installing hypervisor . each vm has its own cpu ,memory,and setup. Vm is separated logically we cannot see this machine therefore it is called vm.
 In this way we are using server space efficiently using devops using hypervisor. 

Example 
ans) 


Int.Q) how will create 10 virtual machines at once? Or what is automation you are using in your oranganization for infrastructure creation

NOTE :  infrastructure == VM== Ec2 
ans)  Tool name = terraform


AWS CDK  cloud development kit( amazon walao ka khud ka tool hi) . Latest 
So there are 4 ways to create infrastructure or ec2 instance


What is os?
ans) os acts a medium or bridg between computer softwares(jerkins,kuber,etc) and computers hardware(mouse,key)so that cs and ch can communicate with each other.

2nd def =  os is useful for establishment of communication between system hardware and system softwares
2) when ever user send a request it goes from softwares to your os then request got to the hardware finally the response received in same way 

User ( req) => os (kernal) = > hardwares 
hardware=> os=> user.




Computer communication lifecycle.

user=>laptop/server=>app(any app)  => os=> hardware and wise versa

Why linux is so popular and mostly used?
ans)


It is free
If is free and open source
It is secure as compare to all os we do need to install antivirus
Its distribution is free like ubuntu
It is very very fast.




Fundamentals of os
ans) given in diagram

Kernel is a heart of os.
What is kernel
ans) The kernel is responsible for managing the hardware and providing essential services to other parts of the system.

imp)4 props of kernal
Device management
Memory  management
Process management
Handling system related calls

Kernel = kernel is a heart of os because it establish the communication between  the system,s hardware and system softwares or app like vs code.
 What is shell ?
ans) shell is way to communicate with os using shell commands.

Diff between /dash and /bash
ams) in linux history /sh redirects to bash but new updated of os like ubuntu uses /dash be default so to execut shell scripts use /bash

/bash /sh / zsh ye sb extension hai commands ko execute krne k liye jese progs langs mait hota hai like indexx.js or index.py

#!/ it is called shebang.


What is shell scripting
ans) the process of automating the day to day activities or regular actives in our linux os isshell scripting.
Ex = making 100s of file and folders 


Terminal vs shell

So, the shell is the engine that processes your commands, and the terminal is the window or interface through which you interact with the shell. The two terms are often used interchangeably, but they refer to different aspects of the command-line environment.

Diff between shell scripting and linux cmds
ans) https://chat.openai.com/share/351fae52-6647-4f9f-af5a-95ed2d3ec25c
Go to this link for all shell shell scripting shell commands
https://chat.openai.com/share/8b7e37ca-f467-4ff1-ba55-696cc2dc4402


NOTE interview ques.




| command send out put of first cmd to second commands
NOTE when we use pipe | command with date it will not work
Becoz date cmd is default system cmd which sends it output to stdin so i this case pipe cmd didnt get out of date so it can pass second command that is echo.
Inshort pipe | cmd send output of one cmd to second cmd.

TRAP cmd = Trap is use to trap signals of linux like to terninat ctrl +c to end the process u can change the function this cmd using trap.


What is shell?
Ans  SSH stands for "Secure Shell," and it is both a protocol and a tool used for secure communication over a network. The SSH protocol is widely used for accessing and managing remote servers securely.





Grep is case sensitive jesa 
Grep searches for patterns
-r flag mtlb pure system mai dund ke laho
-i mtlb case sensitive ,,, DEVOPs essa likha h tho devops esse bi dunde gaa aur DEVOPS esse bi dunde gaaa.



Awk cmd 
awk 'NR>=20 && NR<=100 && /TRACE/ {print $1,$2,$3}' app.log

Container = so the advancement of physical server is vm which uses hypervisor but vm are aslo not used to its full extent so we introduce containers to use vm upto full extent 
2) In containers they do not have there is os they uses os of vm therefore they are so light in weight



Disadvantage of docker = 
Container is made up of docker file to docker image to docker container 
Only single point of disadvantage is docker engine the process from docker file to docker image to docker container is maintain by docker engine if docker engine is failed then all containers will failed this is main advantage
Solution is using buildaa tool.




Backing up cmds






For restore file cmd is == tar -xzvf {filename}


Crontab cmd


*/2 * * * * bash /home/akshay/logs/makingbackup.sh

*/2 * * * * bash /home/akshay/snapchat/makingbackup.sh



















Cred syntax




 withCredentials([usernamePassword(crendentialsId:"dockerhub",passwordVariable:"dockerhubpass",usernameVarible:"dockerhubuser")]){
                 sh " docker login -u ${env.dockerhubuser} -p ${env.dockerhubpass} "
                 sh "docker tag node-aap-test-new:lattest ${env.dockerhubuser}/node-app-test-new:latest"
                 sh "docker push ${dockerhubuser}/node-app-test-new:latest"
                 echo "bhaya code push ho gaya"
                 }




Kubernetes  cluster is a collection master node and worker nodes  in which some service are running which allows k8s to perform effectively.

K8s provide the facility of auto healing and scaling

2) int que : which node allowds commu. Between master adn node
ans) api server node.

What is pod
ans) pod is a smallest unit in k8s in which docker containers runs.

Apps always run inside nodes servers.

What is scheduler
ans) scheduler is a service which is responsible for creating a pod or to manage a pod but it gives instruction to api server then api servcer give to kublet ,then kublet maintain the pods

What is controller manager
ans) cm is a head of master node which keep track of all ther services present in worker node with the help of api server

What is service proxy
ans) sp give access of application to the outside user.
Or

Sp exposes the cluster to outsides users.
What is kubectl
ans) it is like a customer which orders to make containers or clones . it give order to api server ,then api server give this to scheduler then schuler says ok i will give you pods which api server gives to kublet and kublet deploy pods


Auto scaling kese hota hai ?
ans) scheduler maker more pods as per the requirement 
Authealing
Etcd makes zinda kr deta hai mare container ko 


CNI = container network interface 
This network allows master node and worker node and all services to communicate with each other.



What is terraform and ansible?
ans) Certainly! Let's break it down in simple terms:
Terraform:
Terraform is a tool used in the world of computing to help manage and automate the setup of your infrastructure. Imagine you need to create and manage servers, databases, and other resources in the cloud. Doing this manually can be time-consuming and error-prone. Terraform helps by allowing you to define your infrastructure as code. In simple words, you write down in a file how you want your infrastructure to look, and Terraform takes care of making it happen.
Example:
Let's say you want to set up a web server in the cloud. With Terraform, you write a configuration file that says, "I want a server with this much memory, using this operating system, and with these security settings." You run Terraform, and it goes off and creates that server for you. If you later decide you need two servers instead of one, you just change the configuration file, run Terraform again, and it makes the necessary adjustments.
Ansible:
Ansible is another automation tool, but it's more focused on configuring and managing software rather than infrastructure. While Terraform is great for setting up servers and networks, Ansible is excellent for tasks like installing software, changing configuration files, and coordinating different tasks on multiple servers.
Example:
Let's say you have ten servers, and you need to install a specific software package on each of them. Instead of logging into each server one by one and running commands, you write an Ansible playbook (a script) that says, "On all these servers, install this software." You run Ansible, and it takes care of connecting to each server and making sure the software is installed.
In summary, Terraform is used for setting up and managing infrastructure, while Ansible is used for configuring and managing software on that infrastructure. Together, they make a powerful combination for automating and streamlining the management of your IT resources.


=================AWS==========================

On demand instance = jo apn banate hai
On spot instance = jinki boli laganai padti onspot sasta hota hai pr milta nii hai 

 
#####################################################
Sonarcube install cmd = docker run -itd --name sonarqube-server -p 9000:9000 sonarqube:lts-community


################# K8S###############################


Containers do not fullfile the production level requirements so we use k8s 
In container we use cmds(run cmd)  but in pods we use yml file.



This is when in one pod we make two containers they shared network and storage.
Between themselves.



So in deployment it gives us facility of 
Auto scaling (by replica set or replicas controller)
Auto healing (by by replica set controller)
Controller keeps tracks which pod is killing then it will heal it



Depoment always match the desired state which is given in yml file
If i have written 5 replica and by chance replica is 4 then controller will manage and match the desired state in this way it gives us auto healing

—--------------deep dive in k8s concept—---------------







So deploy is just a wrapper on replicaset controller and replicaset controller is wrapper on pod

Underthe hood deploy uses replicaset controller to match the desired state.

Deploy -> replicaset controller -> pod

2) if you delete pod parallely new pods is created at same time without disturbing another pods this is what happens when customer uses our website.



these are facility given by services or svc by k8s

If all traffic goes to one pod it get down
sol) laid balancing . thesvc will distribute the traffic to different nodes eqallly by tracking ip address of each pods

2)But when news pods heal ip addressed is changed so instead of keeping track of ip address it keep track of labels and selectors it is called service discovery

3) most impt exposing to the world 
Cluster ip : inside cluster
Node port : within the organization
Laid balancer : public any one can access only having internet





K8s services missing these 2 points therefore ingress come into the picture 
K8s do not enterprise level supports 
Like sticky = ek user ko ek hi application se stick krke rkna agr usne ek br bi url bheji hai appp mai tho bs vi issi app se attact rahe ga

Tls = security
Path = according to path load balance krna mtlb 
Agr /home hai tho 1st appm jaho agr /abt hai thp app2 mai jaho 
Ratio based load ko distribute krna mtlb 2 idr jaho 5 udr jaho 

2) cloud charge krta tha for each static ip address bhut jyada **


**************************************************************************
What is config map
ans) config map is used in k8s to store data and this data at later point of time this data is used by pod or deployment or by application.

What is secrets 
ans) when we have to save some sensitive info then we store in secrets . what secrets do is its encrypt the data justbefore saving it into in etcd. K8s provided custom encryption but you can use other encryption also . now if hacker hacks the etcd also it the encrypted is of no use of him.


What containers init inside pod yml in k8s?
and) inside pod yml if container init is define then this container will created first and will complete its lifecycle then only other container will be created
2) if two init then also first init will be created and complete its cycle then 2nd will be

Real life example : if inside pod there are 2 con.
Web app con
db
Then db will be connected first then web con will be created.
..


 




