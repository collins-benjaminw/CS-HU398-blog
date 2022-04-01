# Modern Apps and the Cloud
## Benjamin Collins
### CS-HU398

Oh, the cloud. Such a marketing term, right? It's so nebulous, who really knows what it means? Let's deconstruct what the technology actually is, and its implications and uses.

The main physical technology behind the cloud is the datacenter. Any time you read "the cloud is _____" your mental image should be such facilities. Put simply, a datacenter is a large warehouse, housing a massive amount of computers working together to provide bulk services to the internet. The purpose of this blog is not to explain these systems or how they operate, but how they are used, and how their end goal is achieved, though I intend on giving a more indirect explanation on these topics, focusing more on the software built on the cloud than the actual datacenters themselves. 

The main technologies built on and for the cloud that I will cover are chosen from those most important to the role of developer, as that is my perspective:


 - Software as a Service (SaaS)

 - Cloud Platform Systems

 - Infrastructure as code

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

These cloud vendors own and operate multiple datacenters across the US and the world as a whole. This means that they can offer fast and reliable service to customers anywhere. 

## References and Further Reading

## Attributions
