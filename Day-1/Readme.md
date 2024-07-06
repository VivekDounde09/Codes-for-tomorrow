## DAY-1 (5/7/24)

## Web Servers

### Question 1: What Is NGINX?
NGINX (pronounced "engine x") is a free, open-source web server software that can also be used as a reverse proxy, load balancer, mail proxy, and HTTP cache. It was developed in 2004 by Russian developer Igor Sysoev as a competitor to Apache HTTPd. NGINX is designed for maximum performance and stability, and to handle a high number of connections simultaneously.

- NGINX works by using an asynchronous, event-driven approach to handling requests.
- It handles multiple requests in a single worker process, instead of creating a new process for each request. This, along with its non-blocking architecture, makes NGINX fast and scalable.
- NGINX is frequently deployed in Kubernetes stacks, where it acts as a reverse proxy and load balancer to manage incoming traffic to the cluster.
- NGINX also functions as a proxy server for email communications protocols, such as IMAP, POP3, and SMTP.
- It offers features such as user redirection to IMAP or POP3 servers, and user authentication using an external HTTP authentication server.
- It also helps in caching data at edge locations, which helps it to work faster than Apache.

### Question 2: What Is Apache?
Apache is a free, open-source web server that allows users to deploy websites on the internet. It's a project of The Apache Software Foundation, a non-profit organization that maintains many open-source software projects.

- Apache is known for its use of the HTTP/S protocol and is designed to serve static web pages.
- It's fast and secure enough to run major websites, and it supports modern authentication, including internal user lists or external authentication providers.
- Web traffic can also be encrypted with Transport Layer Security 1.2 or 1.3.
- Apache runs on various operating systems, including Linux, Windows, and macOS.
- Apache is flexible and can be customized to your needs, but this can also open up security vulnerabilities. More experienced web developers can avoid these issues, but it can be dangerous for others.

### Question 3: What are the Differences Between Apache and NGINX?
Apache and NGINX are both open-source web servers that can run large-scale applications and are easy to learn. They differ in their architecture, configuration, and performance:

#### Architecture
- Apache uses a process-driven architecture, while NGINX uses an event-driven architecture.
- Apache creates a new thread for each request, while NGINX can handle multiple requests within a single thread. This makes NGINX more resource-efficient and performant than Apache.

#### Configuration
- Apache is decentralized, while NGINX is centralized.
- Apache's distributed configuration uses multiple servers to handle requests together, while NGINX's centralized configuration relies on a single server.

#### Performance
- NGINX's event-driven architecture makes it faster than Apache's process-based architecture.
- NGINX can also provide higher concurrency and performance.


### Question 4: How to Install NGINX in Ubuntu and Basic Configurations?
To install NGINX on Ubuntu and perform basic configurations, follow these steps:

#### Get a Ubuntu Machine
Get a Ubuntu machine on your local system or from providers such as AWS, Azure.

#### Install NGINX
```
sudo apt-get update
sudo apt install nginx
```
Check the List of Every App Profile That You've Made on the Firewall
```
sudo ufw app list
```
Check Your Web Server
```
systemctl status nginx
```
Stop Your Web Server
```
sudo systemctl stop nginx
```
Start Your Web Server
```
sudo systemctl start nginx
```
Restart Your Web Server
```
sudo systemctl restart nginx
```
Disable NGINX from Starting Automatically on Boot

```
sudo systemctl disable nginx
```
Re-enable the Service to Start Up at Boot

```
sudo systemctl enable nginx
```







