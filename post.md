So I’m sure you’ve heard one or more of these terms in the last twelve months. They are hot topics to be talking about but why are we talking about these terms together?

Because they are the perfect storm of amazing technologies that allow us to build highly distributed, composite and scalable applications in today’s world and I wanted to talk a bit about them.

## Microservices

The concept fo microservices has been around for a long time but only recently has the term become mainstream in technology discussion. If we back up a bit, in the old days we had very large and coupled applications that were difficult or impossible to integrate with. Large single binaries, shipped with out applications, unable to work with other languages or platforms. Then we introduced service oriented architecture (SOA) principles which promoted exposing this functionality over the wire via HTTP or TCP which are common protocols. But still, these applications were very monlithic in nature, difficult to deploy, difficult to rebuild and so forth.

Now enter [microservices](http://martinfowler.com/articles/microservices.html).

In order to minimize the brittleness of our services, we need to break them down into smaller units. This minimizes upstream dependency issues, concerns with frequent deployments, language lock-in. In the world of true microservices you can assume that every endpoint of a service would be deployed as it’s own service. For example, you may have one service that capitalizes a string, one that reverses a string, and one that pluralizes a string. Typically you’d build an application and write three service endpoints that you’d deploy together. Now these are all seperate decoupled services that depend on each other via common transport and protocol such as HTTP and JSON.

Typical languages and application stacks don’t really promote this type of architecture since they are monolithic themselves, and the frameworks such as ASP.NET or Spring come with mostly prebuilt conventions of how you build larger n-tier style applications and services.

This is where Node.js really shines in regards to microservices.

## Node.js

At it’s core [Node.js](https://nodejs.org) is an extremely light platform that’s driven by a passion community by open source modules. This modular system is what allows you to build loosely coupled and scalable systems that talk over HTTP and JSON since these are built right into Node.js. So this modular architecture goes nicely hand in hand with micrservices.

Think about deploying components rather than applications.

As you can imagine, maintaining a smaller component is much easier to do than a large service application. It’s easier to break up the responsibility amongst engineers. It’s easier to rebuild or refactor a component and to convince the business of this. You also have to coordinate at a much larger level with dependent teams since so many changes could be rolled out with a larger application than a smaller component. I think you see the point I’m trying to make here.

## Containers

Assuming you migrate 10 monolithic service applications to 100 independent micro services, you will run into some concerns. The primary one is management of these 100 services. As an engineer, how do you manage them all running locally in development mode? How do you ensure you’ve always got the latest versions locally? What about deploying to production and ensuring they’re all configured and talking smoothly?

Containers to the rescue! Well, [Docker](http://docker.com).

If you haven’t been paying attention the last year, Docker is a really awesome platform that allows you to configur and run applications via application containers. This is a shift from virtual machines where each application needed to run on a full operating system. With containers, you are sharing resources on the host operating system with proper security, file, networking resources managed for you.

The awesome thing with Docker is the application stack you configure and run locally is the exact same that you can run in production. Repeat, the exact same configuration locally as in production.

So how does this pertain to microservices and Node.js? Docker now becomes your platform to configure and manage all of these applications. They are configured and provisioned all together and you can essentially script out this process to make provisioning a complete microservices stack locally with one click. You can manage this with tools like [Docker Compose](https://github.com/docker/compose).

## Conclusion

It’s an exciting time to be an engineer. Configuring, Building, Testing and Deploying applications is entering a new age and it’s really going to be awesome.

One thing to keep in mind is this is a big architecture shift. It’s not easy as just breaking down your services, calling them a microservice and calling it a day. There is additional work that goes into ensuring you properly manage these smaller components but the benefits are going to outweight the cons once you get it right. Your infrastructure will operate at higher efficiency, your engineers will be happy and you get to break down the silos.