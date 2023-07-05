![Alt text](https://i.imgur.com/cbvK6DQ.jpeg)

Explanation of the infrastructure:

Server: A server that hosts all the components of the web infrastructure.

Web Server: We install and configure Nginx as the web server on the server. Nginx will handle incoming HTTP requests from users.

Application Server: We install an application server. The application server will be responsible 
for executing your code base and handling dynamic content generation.

Application Files: Add a code base to the server and include all the files required to run your website/application.

Database: We install and configure MySQL as the database management system on the server. 
The database will store and manage the website/application data.

Domain Name: Start to configure the domain name "foobar.com" with a DNS record. Add a "www" record that points to your server's IP address,
which in this case is 8.8.8.8.

Specifics about the infrastructure:

What is a Server:
A server is a software or hardware device that accepts and responds to requests made over a network.
The device that makes the request, and receives a response from the server, is called a client.

What is the role of the domain name:
The domain Names are used for different purposes, including application-specific naming, addressing,
and in various networking contexts to establish: – Simple identification of hostnames and hosts.

What type of DNS record is "www" in www.foobar.com: The "www" is a subdomain, and in this case, it is a CNAME (Canonical Name) record.
The CNAME record points the "www" subdomain to the main domain (foobar.com).

What is the role of the web server:
The primary role of a web server is to store, process, and deliver requested information or webpages to end users.
All website data is stored on a physical web server to ensure its safety.

What is the role of the application server:
The application server is responsible to the user authentication and security,processing and serving HTML files
processing and compiling JSP files with help from its servlet/JSP engine, then serving the entire response generated back to the browser.

What is the role of the database:
The intention of SQL (often pronounced sequel) is to store, retrieve, manage and manipulate data within a database management system.

What is the server using to communicate with the computer of the user requesting the website:
The server communicates with the user's computer over the Internet using the HTTP protocol. When the user requests the website,
the server sends back the corresponding HTML, CSS, and other assets to be rendered by the user's browser.

Issues with this infrastructure:

SPOF:
A SPOF(Single Point of Failure) or single point of failure is any non-redundant part of a system that,
if dysfunctional, would cause the entire system to fail.

Downtime when maintenance:
When performing maintenance tasks like deploying new code, the web server needs to be restarted, resulting in temporary downtime.
To minimize this, you can use techniques like rolling deployments or load balancers to ensure continuous availability while updating the system.

Cannot scale if too much incoming traffic:
With a single server, this infrastructure may struggle to handle a high volume of incoming traffic. To scale the system, you can introduce load balancers,
additional servers, or cloud-based solutions that allow horizontal scaling.
 
