## Secured and monitored web infrastructure


<img src="https://e-ticaret-dadas.s3.eu-north-1.amazonaws.com/Untitled-2024-02-22-0904+(4).png">
<h2>Written by Dadash Huseynzade</h2>
<i>Designed three server web infrastructure that hosts the website www.foobar.com, it must be secured, serve encrypted traffic, and be monitored.</i>

<h3>1 - Firewalls</h3>
<p>Firewalls are added to control and monitor incoming and outgoing network traffic based on predetermined security rules. They help protect the infrastructure from unauthorized access, malware, and other cyber threats.</p>
<h3>2 - Why is the traffic served over HTTPS</h3>
<p>Traffic is served over HTTPS to encrypt data transmitted between clients and the server, providing confidentiality, integrity, and authentication. This helps prevent eavesdropping, tampering, and man-in-the-middle attacks</p>
<h3>3 - What monitoring is used for</h3>
<p>Monitoring is used to track the performance, availability, and security of the infrastructure and applications. It helps identify issues, optimize resources, and ensure reliability and compliance.</p>
<h3>4 - How the monitoring tool is collecting data</h3>
<p>The monitoring tool collects data by periodically querying system metrics, application logs, and network traffic. It may use agents installed on servers or APIs provided by the infrastructure and applications to gather information.</p>
<h3>5 - Monitoring Web Server QPS</h3>
<p>To monitor the web server's queries per second , you can configure the monitoring tool to collect and analyze HTTP request logs or use server-side monitoring agents to track server performance metrics.</p>

<h2>What the issues are with this infrastructure?</h2>
<b>Why terminating SSL at the load balancer level is an issue</b> - <span>Terminating SSL at the load balancer means that the SSL encryption is decrypted at the load balancer before being forwarded to the backend servers. While this simplifies SSL certificate management and offloads CPU-intensive encryption tasks from backend servers, it also introduces a potential security risk. The communication between the load balancer and backend servers is no longer encrypted, which could expose sensitive data to interception if the internal network is compromised</span>.<br>
<br>
<b>Why having only one MySQL server capable of accepting writes is an issue</b> - <span>  Firstly, it creates a single point of failure. If the MySQL server fails, all write operations will be disrupted, leading to downtime and potential data loss. Additionally, it can limit scalability since a single server can only handle a limited amount of write traffic. This setup also poses challenges for high availability and disaster recovery, as there's no failover mechanism in place to automatically switch to a backup server in case of failure.</span>.<br>
<br>
<b>Identical Servers with All Components</b> - <span>Firstly, it can lead to resource underutilization if the workload distribution is uneven. For example, if the database server is underutilized while the web server is overloaded, resources are wasted. Secondly, it lacks flexibility in scaling individual components independently. For instance, if the database server requires more resources due to increased workload, scaling up all servers may not be cost-effective</span>.<br>
