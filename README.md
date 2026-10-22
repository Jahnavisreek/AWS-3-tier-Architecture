# AWS-3-tier-Architecture
Implementation of a three-tier web application architecture using AWS services
![Uploading architecture-diagram.png.png…]()


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
