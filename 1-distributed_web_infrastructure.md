## Distributed web infrastructure

<img src="https://e-ticaret-dadas.s3.eu-north-1.amazonaws.com/Untitled-2024-02-22-0904+(3).png">
<h4>Written by Dadash Huseynzade</h4>
<i>As you can see I have three server. Why I create this chart-flow because I want to show you it how to work load balancer and why is it important the big company.</i>

<h3>1 - I would to explain what is the load balancer</h3>
<p>The load balancer improves performance by evenly distributing requests among the servers, preventing any single server from becoming overwhelmed. <br> Adding a load balancer (HAproxy) ensures efficient distribution of incoming traffic across multiple servers, enhancing reliability and scalability.</p>
<h3>2 - Why I configured round-robin distribution algorithm</h3>
<p>Configuring the round-robin distribution algorithm ensures that incoming requests are evenly distributed across all available servers. This approach helps to maximize resource utilization and prevent any single server from being overwhelmed with traffic. By cyclically routing requests to each server in turn, round-robin load balancing promotes fairness and avoids potential bottlenecks, thereby enhancing overall system performance and reliability</p>
<h3>3 - Explaining Active-Active or Active-Passive setup  load-balancer</h3>
<p>In an Active-Active setup, both load balancers are actively distributing traffic simultaneously. This setup increases fault tolerance and scalability, as both load balancers share the traffic load. In contrast, an Active-Passive setup involves one active load balancer handling traffic while the other remains idle, serving as a backup. Active-Passive setups are simpler but may experience downtime during failover</p>
<h3>4 - How a database Primary-Replica (Master-Slave) cluster works</h3>
<p>A database Primary-Replica (Master-Slave) cluster involves one primary node (master) and one or more replica nodes (slaves). The primary node handles all write operations, while replica nodes replicate data from the primary node and handle read operations. This setup improves fault tolerance, scalability, and performance.</p>
<h3>5 - What is the difference between the Primary node and the Replica node in regard to the application</h3>
<p>The primary node accepts write operations and is responsible for maintaining the authoritative copy of the data. Replica nodes replicate data from the primary node and handle read operations, serving as backups and improving read scalability.</p>

<h4>What the issues are with this infrastructure?</h4>
<b>Single Points of Failure (SPOFs)</b> - <span> may exist in the absence of redundancy for critical components like the load balancer or database</span>.<br>
<b>Security issues </b> - <span> arise from lacking a firewall and HTTPS, potentially exposing the system to unauthorized access and data breaches</span>.<br>
<b>No monitoring</b> - <span>Lack of monitoring leaves the infrastructure vulnerable to performance issues, failures, and security breaches without real-time visibility into system health and activity</span>.<br>
