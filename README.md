# SpringTabloid
A tabloidic resource for spring boilerplate
* Service Discovery (Eureka)
* Circuit Breaker (Hystrix)
* Intelligent Routing (Zuul)
* Client-Side Load Balancing (Ribbon)

# Monolith to Microservices :
 * The Twelve Factors
 * Codebase
 * Dependencies
 * Config
 * Backing Services
 * Build, Release, Run
 * Processes
 * Port Bindings
 * Concurrency
 * Disposability
 * Dev/Prod Parity
 * Logs
 * Admin Processes
 
# Leonard Richardson’s Maturity Model

## Representational State Transfer (REST) 
REST was originally advanced by Dr. Roy Fielding as part of his doctoral dissertation in 2000. Fielding helped define the HTTP specification and wanted to help illustrate how the web—an already proven, massively scalable, decentralized, failure-resistant fabric—could be used to build services. HTTP is an existence proof of the REST architecture’s merits.

Where previous approaches to distributed services (like CORBA, EJB, RMI, and SOAP) focused more or less on exposing an object-oriented interface and methods as a remotely accessible service (RPC), REST instead focuses on the manipulation of remote resources or entities. Nouns, not verbs. Entities, not actions.
REST is all about exposing the mutations of business state with the verbs (GET, PUT, POST, DELETE, etc.) and idioms (HTTP headers, status codes, etc.) that HTTP already gives us to support service-to-service communication. The best REST APIs tend to exploit more of HTTP’s capabilities. REST, for all of its benefits, is an architectural constraint on HTTP, not any sort of standard, and so we’ve seen a proliferation of APIs of varying degrees of compliance with RESTful principles. Leonard Richardson put forth his REST maturity model to help grade an API’s compliance with REST’s principles:

Level 0: The swamp of POX
(Naturally, it would be zero-indexed!) Describes APIs that use HTTP as a transport and nothing more. SOAP-based web services, for example, use HTTP, but they could as easily use JMS. They are, incidentally, HTTP-based. Such a service uses HTTP mainly as a tunnel through one URI. SOAP and XML-RPC are examples. They usually use only one HTTP verb (POST).

Level 1: Resources
Describes APIs that use multiple URIs to distinguish related nouns, but otherwise avoid the full features of HTTP.

Level 2: HTTP verbs
Describes APIs that leverage transport-native properties (like HTTP verbs and status codes) to enhance the service. If you do everything incorrectly with Spring MVC or JAX-RS or any other modern-day REST framework, you’ll still probably end up with an API that’s level 2 compliant! This is a great starting point.

Level 3: Hypermedia controls (HATEOAS, for Hypermedia as the Engine of Application State)
Describes APIs that require no a priori knowledge of a service in order to navigate it. Such a service promotes longevity through a uniform interface for interrogating a service’s structure.
