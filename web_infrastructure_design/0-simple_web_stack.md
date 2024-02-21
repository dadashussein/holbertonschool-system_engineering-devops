## Simple web stack - LAMP stack

<img src="https://e-ticaret-dadas.s3.eu-north-1.amazonaws.com/photo_2024-02-21_17-07-51.jpg">

#### I am  able to explain some specifics about this infrastructure:
**-   What is a server :** 
A server is a computer or software that provides services to other computers  over a network.

  **- What is the role of the domain name:**
 The domain name serves as the address for a website, allowing users to easily find the human-readable name  instead writing IP address on the internet
 
 ****-   What type of DNS record  `www`  is in  `www.foobar.com`:****
 The "www" in "[www.foobar.com](http://www.foobar.com/)" typically refers to a hostname, commonly used to indicate the web server for a website. It is typically associated with an "A"  DNS record pointing to the IP address of the web server.
 
 **-   What is the role of the web server:**
 The web server delivers web content to users' browsers in response to their requests, facilitating the hosting and serving of websites, web applications, and other online resources.
 
 **-   What is the role of the application server:**
 The application server runs the backend logic and processes for web applications, handling tasks such as data processing, business logic, and database interactions.
 
**-What is the role of the database:**
The database stores, organizes, and manages data for an application, allowing for efficient retrieval, manipulation, and storage of information

**-What is the server using to communicate with the computer of the user requesting the website:**
Hypertext Transfer Protocol (HTTP)


#### I am be able to explain what the issues are with this infrastructure
- **SPOF**: If any critical component fails, the entire system may become inaccessible. 
- **Downtime during Maintenance**: When maintenance tasks like deploying new code or restarting the web server are necessary, the website may experience downtime, impacting user access.
- **Scalability Limitations:** If there's a sudden surge in incoming traffic, the infrastructure may struggle to handle the load efficiently, leading to slow performance or crashes