# AWS-3-tier-Architecture
Implementation of a three-tier web application architecture using AWS services

<img width="1792" height="2400" alt="architecture-diagram png" src="https://github.com/user-attachments/assets/5fbf51e5-b9b9-4714-bab8-8092efada3a6" />

## Repository Structure

```text
3tier-app-deployment-aws-main/
│
├── 3-Tier Architecture Application Steps   # Documentation / walkthrough notes
├── error                                   # Error logs or debugging notes
├── image                                   # Architecture diagram / preview image
├── install.sh                              # Shell script for automated dependency/system setup
│
└── application-code/
    ├── nginx.conf                          # Reverse proxy & web server configuration
    │
    ├── web-tier/                           # Presentation Layer (Frontend - React.js)
    │   ├── public/                         # Static HTML, icons, assets
    │   ├── src/                            # React components, styles, logic
    │   ├── package.json                    # Frontend dependencies & build scripts
    │   └── README.md                       # Frontend documentation
    │
    └── app-tier/                           # Application / Logic Layer (Backend - Node.js)
        ├── DbConfig.js                     # Database connection string & setup
        ├── index.js                        # Server entry point (API routing / Express server)
        ├── TransactionService.js           # Business logic & database operations
        ├── package.json                    # Backend dependencies (e.g., Express, DB drivers)
        ├── package-lock.json               # Exact dependency versions
        └── README.md                       # Backend documentation
```

## Architecture

The application is organized into three logical tiers:

1. **Presentation Tier:** Handles incoming web requests and serves the user-facing interface.
2. **Application Tier:** Processes application requests using Node.js.
3. **Database Tier:** Uses Amazon RDS for MySQL to manage relational data.

The AWS networking components control how traffic reaches the application and how the different tiers communicate.

---
## Technologies Used

### Compute and Application
* **Amazon EC2**
* **EC2 Auto Scaling Groups**
* **Node.js**
* **Nginx**
* **HTML**

### Networking and Security
* **Amazon VPC**
* **Public and Private Subnets**
* **Internet Gateway**
* **NAT Gateway**
* **Security Groups**

### Traffic Management and Domain Configuration
* **Application Load Balancer (ALB)**
* **Amazon Route 53**
* **AWS Certificate Manager (ACM)**

### Database
* **Amazon RDS for MySQL**

---

## Implementation Steps

1. Configured the VPC and required public and private subnets.
2. Configured Internet Gateway, NAT Gateway, and security groups.
3. Deployed the application on EC2 instances.
4. Configured the Auto Scaling Group and Application Load Balancer.
5. Set up the Node.js application and Nginx web server.
6. Configured Amazon RDS for MySQL.
7. Configured Route 53 and ACM for domain and certificate management.
8. Tested application accessibility and end-to-end connectivity.

---

## Screenshots
<img width="1908" height="913" alt="VPC Resource Map" src="https://github.com/user-attachments/assets/b5cc5500-f7a8-42fd-8495-9ffbf044ac36" />
<img width="1917" height="1012" alt="Screenshot 2026-10-16 195443" src="https://github.com/user-attachments/assets/5aa5067a-ac93-4d4d-bbf6-7e425f00abe5" />



| Working Application | AWS Configuration |
| :---: | :---: |
| <img width="1917" height="965" alt="final" src="https://github.com/user-attachments/assets/d565e6ea-f429-4743-92e2-11e50161b0fd" /> |

---

## Key Learnings

* AWS networking and subnet design
* EC2 deployment and instance management
* Load balancing and Auto Scaling
* Web server configuration using Nginx
* Node.js application deployment
* Managed MySQL database configuration
* DNS and SSL/TLS certificate management

---

## Future Improvements

* [ ] Infrastructure provisioning using Terraform
* [ ] CI/CD automation using Jenkins or GitHub Actions
* [ ] Application containerization using Docker
* [ ] Monitoring and logging setup using Amazon CloudWatch
