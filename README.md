# Interview_Questions
# Sirius-BI Questions<br></br>
# Round 1
Q1: Ma jata hu aur website ka naam likhta hu but its not reachable but when I type ip it is reachable?<br></br>
Q2: AWS scretes management?<br></br>
Q3: Abhi service aik vendor provide kr rha ha but unho nay services ko apney infra pay shift karna ha tou kaisey karein ge?<br></br>
A: Blue, Green Deployment Concept<br></br>
Q4: Aik container chal rha ha aur wo container memory aur cpu boht ziada use kr rha ha aur mainey usey constraint karna ha?<br></br>
A: Resource Limit and Resource Usage Concept in Kubernetes<br></br>
Q5: lambda function kay ander aik cheez hoti ha forget wo kia hoti ha?<br></br>
A: Jo lambda functions chal rhy hotey hain un may aik time function/constraint hotey hain usey forget boltey hain (is question ko gpt say aur verify karein)<br></br>
Q6: What is the difference between and add and copy in dockerfile?<br></br>
A: COPY just copies files from the local system into the image, while ADD can also extract archives and download files from URLs. In practice, COPY is preferred because it is more predictable.<br></br>
Q7: Sometimes pipelines failed due to permission error. Why does this issue occur and how to resolve it?<br></br>
A: sometimes cache save ho jati ha server pay tou ap ko jo wo path deti ha us may ja kay cache remove kartey hain sudo rm –rf <br></br>
Q8: Kubernetes may aik pod ha ya aik container ha wo crash backoff may phasa hua ha?<br></br>
A: kubectl logs, kubectl describe pods <pod-name>, akser ye error is wajha say hota ha kay humney image ka naam ghalat define kr diya ha..<br></br>
Q9: Difference between Security groups and NACL's?<br></br>
Q10: What is the difference between layer4 and layer 7 load balancer?<br></br>
A: Load balancers distribute incoming traffic across multiple servers, but they operate at different layers of the OSI model, which affects how they make decisions.<br></br>

🔹 Layer 4 Load Balancer (Transport Layer)<br></br>

How it works:<br></br>

Operates at Layer 4 (TCP/UDP).<br></br>

Makes routing decisions based on IP address, port number, and protocol.<br></br>

Does not inspect the actual data (payload) of packets.<br></br>

Key characteristics:<br></br>

Fast and efficient (low latency)<br></br>

Protocol-based routing only<br></br>

No understanding of HTTP/HTTPS content<br></br>

Example use cases:<br></br>

Simple TCP/UDP traffic distribution<br></br>

High-performance applications where speed matters<br></br>

Examples:<br></br>

TCP load balancing in NGINX (stream module)<br></br>

AWS Network Load Balancer (NLB)<br></br>

🔹 Layer 7 Load Balancer (Application Layer)<br></br>

How it works:<br></br>

Operates at Layer 7 (HTTP/HTTPS).<br></br>

Inspects application-level data such as:<br></br>

URL path (/api, /login)<br></br>

HTTP headers<br></br>

Cookies<br></br>

Hostnames<br></br>

Key characteristics:<br></br>

Content-aware routing<br></br>

Supports SSL termination<br></br>

Can perform advanced features like caching, authentication, and rate limiting<br></br>

Slightly higher latency than L4<br></br>

Example use cases:<br></br>

Routing traffic based on URLs or domains<br></br>

Microservices and API gateways<br></br>

Web applications<br></br>

Examples:<br></br>

NGINX, HAProxy<br></br>

AWS Application Load Balancer (ALB)<br></br>

# Round 2<br></br>
Q: Dockerfile likhwai manually<br></br>
Q: DevOps kia hota ha ? Ye kaam tou aik IT wala banda bhi kr sakta ha tou phir devops engineer hi kyu chahiye ? MyAns: server wagera manage karna hota ha InterviewerReply: Acha btao server may kia manage karna hota ha?<br></br>
Q: Linux ka aik tool ha logs dekhney wala btao wo kia ha aur logs kaisey dekhtey ?<br></br>
Q: Apney aik app deploy ki aur 5 min baad us pay 500 internal server error a gya ap kis tarha us ko solve kro gay?<br></br>
Q: Ma google.com hit karta hu step by step btao peechey kia hoga?<br></br>
Q: What is difference between VM and docker? <br></br>
Q: Meri aik file ha 256GB ki you jb ma VM pay ya docker pay use karta hu us nay tou 256 GB hi consume karna ha then why not you choose VM and why you choose docker?<br></br>
Q: aik app deploy ki ha us ka pdf preview show nhi ho rha kaisey set kro ge?<br></br>
Q: I am using Loadbalancer in aws for 4 instances and i want my 20% traffic to go on instance 1, 30% traffic to go on instance 2, 25% traffic to go on instance 3 amd 25% traffic to go on instance 4. how this thing can be achieved?<br></br>
Q: What are ingress services?<br></br>
