The architecture uses an internet-facing Application Load Balancer deployed in two public subnets to evenly distribute traffic. 
EC2 instances run inside two private subnets and are launched through an Auto Scaling Group for high availability across multiple AZs. 
Incoming user requests first reach the ALB, which forwards traffic only to healthy EC2 instances in the private subnets. 
A NAT Gateway allows private instances to download updates without exposing them to the internet. 
Security groups ensure that only the ALB can access EC2 instances, improving security while maintaining availability.

2. Screenshots of:
a) ALB configuration
<img width="1887" height="702" alt="loadblancer" src="https://github.com/user-attachments/assets/4cdcbce6-beb7-4833-a7e7-d979912f131c" />
b) Target group
<img width="1915" height="735" alt="taggetgroup" src="https://github.com/user-attachments/assets/c8422a93-5238-44ad-b292-986f45547b88" />

c) Auto Scaling Group
<img width="1907" height="652" alt="autoscaling" src="https://github.com/user-attachments/assets/42bc60b1-0124-458c-9ff4-9af42d22b70f" />


d) EC2 instances launched via ASG
<img width="1918" height="747" alt="instances" src="https://github.com/user-attachments/assets/1698e45b-80d6-4b6b-bbac-fbcca0904477" />

