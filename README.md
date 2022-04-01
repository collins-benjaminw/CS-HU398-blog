# Modern Apps and the Cloud
## Benjamin Collins
### A blog written for CS-HU398 at Boise State University

Oh, the cloud. Such a marketing term, right? It's so nebulous, who really knows what it means? Let's deconstruct what the technology actually is, and its implications and uses.

The main physical technology behind the cloud is the datacenter. Any time you read "the cloud is _____" your mental image should be such facilities. Put simply, a datacenter is a large warehouse, housing a massive amount of computers working together to provide bulk services to the internet. The purpose of this blog is not to explain these systems or how they operate, but how they are used, and how their end goal is achieved, though I intend on giving a more indirect explanation on these topics, focusing more on the software built on the cloud than the actual datacenters themselves. 

The main technologies built on and for the cloud that I will cover are chosen from those most important to the role of developer, as that is my perspective:


 - Software as a Service (SaaS)

 - Cloud Platform Systems

 - Infrastructure as code (IaC)

## Software as a Service

Software is that thing you download, install, and run on your machine, right? That used to be the only way users could interact with software. Running applications on the client's infrastructure is useful and sometimes necessary for many types of applications, but for many others, there are reasons not to run applications client-side. There are many reasons to run SaaS over client-side applications, but are just a couple examples:

- Security: imagine trying to keep confidential data away from middle-men. Now imagine all that data gets sent over the internet, with the only real security being https, which while secure, has limitations. Or maybe, your application has to interface with secure data that even the client shouldn't have direct access to. What then?

- Connectivity: let's say your software needs to send requests to other servers, and relies on the speed of those communications to function properly. Since we can't rely on the users to have the fastest internet, we need a better solution.

The clear solution to these problems is to run the applications on a secure and high-networked computer, like a server. Now, you can build your own server and pay for your own high-speed internet and ensure your own security, but Cloud Platforms make it much easier to get up-and-running without these concerns.

## Cloud Platforms

If you're here reading this article, you've probably heard of at least one of the following:

- Azure: Microsoft's cloud platform

- AWS: Amazon Web Services

- Google Cloud: If you're having trouble parsing this one, I'm not sure how you've made it this far on this page.

These cloud vendors own and operate multiple datacenters across the US and the world as a whole. This means that they can offer fast and reliable service to customers anywhere. I'm sure it's clear from the discussion on SaaS that these platforms run your applications in the cloud for users to connect to, but beyond being a big partitioned server, what do these offerings entail?

Well, beyond the larger capacity of resources, and lower cost than building or renting an entire server for your own processes, there are vast feature-sets given by each offering. As my experience is with Azure, I will briefly cover features provided by them and any analogues by the other companies. This is not to say any service is better than another, and devs with primary experience in another platform would absolutely consider their platform first when listing these resources.

- [Azure Web Apps](https://azure.microsoft.com/en-us/services/app-service/web/) are the main feature-rich platform for deploying software to azure. These interface directly with CI/CD pipelines for seamless deployment, and contain an array of monitoring and built-in services to get web apps rolling.
	
	- Similar to: [AWS Amplify](https://aws.amazon.com/amplify/)
	- Similar to: [Google Cloud App Engine](https://cloud.google.com/appengine)

- [Azure SQL Databases](https://azure.microsoft.com/en-us/products/azure-sql/database/): Most every modern application needs storage for its processes, and putting your storage alongside your app makes it as fast as possible.
	- Similar to: [Amazon RDS](https://aws.amazon.com/rds/)
	- Similar to: [Google Cloud Databases](https://cloud.google.com/products/databases)

- [Azure Functions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview): (NOTE: admittedly it's probably best to note that this feature is a response to Amazon Lambda, who was the first major player with this type of integration.) Functions allow you to run certain methods, like the functions of an app, without the overhead of a standard app. This allows for very simple implementations of scheduled tasks, middleware, and simple tasks that can be developed quickly.
	- Similar to: [AWS Lambda](https://aws.amazon.com/lambda/) (AWS is far and away the leader in this category)
	- Similar to: [Google Cloud Functions](https://cloud.google.com/functions)

Now, I could get carried away with every feature these services have, so I'll put a link with further reading below, but it is clear by now that there are services for a development team's every need to deploy applications to the cloud.

This is not even to mention pricing, which depending on the runtime of your application could be as little as a couple dollars a year.

## Infrastructure as code

IaC is a concept that was built *for* the cloud. As shown above, in the cloud, there are resources that are developed as part of a solution. These resources can be built through web portals, but for anything larger than a proof-of-concept, I highly recommend setting up infrastructure with an IaC provider. The number-one system for IaC, and the one I use in my career, is [Terraform](https://www.terraform.io/). Now, there are others, but there are differences between different providers that are large enough that I simply could not explain all the types and what they do differently from one another, so I'll stick to terraform as it's the most obvious way to go about IaC in my view.

IaC as a concept allows you to manage configuration on your cloud resources, called infrastructure. The main idea is that if anything happens to your resources, they can be fixed or rebuilt, then deployed to without worry. This also allows for configuration to be set up in a test environment, then copied with minimal changes to a production environment without unknown factors or human error.

In Terraform, you have configuration written in it's own format similar to json, and does a similar thing to json too, allowing you to build resources as objects that are messaged to an agent in the cloud that reads the configuration on your resources, tracks differences, builds missing resources, updates configuration, and deletes resources you've removed from configuration. A repository of terraform files can be deployed through a CI/CD pipeline to deploy changes to the cloud infrastructure.

## Final word

Overall, these are some of the aspects of modern cloud computing that have interested me as a developer. Working with these technologies has shown me just how powerful the cloud is, and how much trouble it can save you. Overall, I'm excited for the future of this technology.

## References and Further Reading

- [Azure](https://azure.microsoft.com/en-us/)
- [AWS](https://aws.amazon.com/)
- [Google Cloud](https://cloud.google.com/)
- [Terraform](https://www.terraform.io/)
