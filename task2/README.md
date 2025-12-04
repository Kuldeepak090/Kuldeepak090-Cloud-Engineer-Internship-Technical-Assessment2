The EC2 instances are launched in private subnets through an Auto Scaling Group using a launch template that automatically installs and configures Nginx. 
User data updates the OS, installs Nginx, enables it at boot, and deploys the resume page in the web root directory.
The ALB handles all incoming public traffic and forwards it securely to private instances. 
Basic hardening is applied by restricting inbound traffic using security groups, isolating instances in private subnets, and allowing only the ALB to communicate with them.

2. Screenshot of: 
a) EC2 instance
<img width="1907" height="752" alt="Screenshot 2025-12-04 200948" src="https://github.com/user-attachments/assets/00b4457b-2e80-4d80-a53f-b4bec4a3619e" />

b) Security Groups
<img width="1896" height="743" alt="securit_group" src="https://github.com/user-attachments/assets/ca747758-56e7-43fd-9cf0-6753a80a7836" />

c) Website accessible in browser
<img width="1918" height="965" alt="website" src="https://github.com/user-attachments/assets/a7101494-4cba-448b-a422-8cf1cd24aa7d" />
