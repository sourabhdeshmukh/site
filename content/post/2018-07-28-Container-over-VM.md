{
    "title": "Container Over VM",
    "date": "2018-07-28",
    "categories": ["Docker"],
    "tags": ["VM", "Docker", "Containers"]
}


In these post I am going to brief you about the containers. Container is like a VM, I am not denying that but they are not VM. Consider if we want to install and run application in two different VMs, we need to download binary of that applications which might have other dependencies apart from which already present inside binary. After downloading we need to install it which will install the application as well as it will check for dependencies, if they are present then only it will get install or sometimes what happens with some apps they get install but denies to run due to lack of dependencies. If Application is perfectly running on one VM and we want to run that application on to another VM we need to perform same procedure which I mensioned above, and if all requirements are satisfied then only app will successfuly execute. Here problem is that we need to search and install packages when we want to run separate VM.  

Another problem is that the binary which we downloaded might support on system os or it will face system environment problem, to overcome this problem containers are used.  

If we only ship the application code or binary, then we cannot be sure, as each environment might be different. But if we can ship the application with its code along with its dependencies in a box to different environments, which everyone know, how to unbox and run the application in an isolated and secured away. Then things would work out. That is what the container's actually do. Container's creates execution environments.  

Containers are application-centric way to deliver high-performing, scalable applications on the infrastructure of your choice. Containers with microservices make a lot of sense here because we can do rapid development and deployment with confidence.Using containers we can also record a deployment by building an immutable infrastructure. if something goes wrong with our new changes, we can always come back to old known working state. Containers are cost effective than any other deployment methods available now. By all this information you might think that container is lightweight VM but they are not as Both provide isolation & run our application, but the underlying technologies they use are completely different. Managing them is also different.

[![HexchatNetworkList](/images/diff.jpg)](/images/diff.jpg)

VM is created on top of the hypervisor which is installed on the host operating system. Hypervisor emulates the hardware like CPU, Memory, Disk etc. from the available resources on the host system. A guest OS like Linux, Windows then gets installed on top of the emulated hardware. We put our application on top of those VM. An application has to go through the guest operating system to reach to the external world.  
Whereas,  
Containers directly run on the host operating system without any guest operating system of its own. Host operating system provides isolation and does resource allocation to individual container.  

**Benefits of containers :**  
1. They are very cost effective.  
2. Platform Independent  
3. Rapid application development  
4. Version Control  
5. Sharing and security  

To deploy application, you might be using the VM. But now the same application can be deployed in a container. A container runs as a process on the host system which takes very less resources as compared to VM. Due to that we can increase the density of applications on that same hardware. We can run same image on different platforms like bare-metal, virtual machine, cloud etc. and get the same consistent experience. Images can be versioned and shared easily. Containers get isolation from the host system so that they don't interfare with one another.  

**Use-cases of Containers :**  
1. Quick Prototyping of Ideas  
2. DevOps  
3. Continuous Integration and Deployment(CI/CD)  
4. Platform as a Service  

With containers we can prototype any ides, as with the right tooling and connecting containers require very little or no efforts. Containers are becoming the unit of execution through which we can get predictable Dev, QA and OPs environment. We can use containers in doing continuos integration and deployment. As we deploy applications with containers. Using them in Paas has become the default choice. For example Red Hat's OpenShift v3, Heroku are built on container technologies.  

Now the question arises is that where to deploy containers?  
Should I deploy them on VM, BareMetal, Cloud etc. From the container's perspective it does not matter as it can  run anywhere. But from the perspective of a company's IT department, the answer is "It depends". There are just so many variables which affect the decision like cost, performance, security, current skill set.  
