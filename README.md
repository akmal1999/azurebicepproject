# azureproject
This project is built based 
"Evaluation Project: Bicep
Objective
Establish a secure and scalable Azure environment tailored for a web application hosted on a Virtual Machine (VM), ensuring high availability, automated deployment, security, and monitoring. The setup must use Bicep for infrastructure definition and include both an Azure SQL Database and a Storage Account, with configurations and deployment processes documented and pushed to a public GitHub repository."

Project Info.

This project is modularized for future expansion and to templatize and organize for future usage.
The modules folder contains subfolders for each logical grouping of resources (like network, compute, data, and core). This makes it easier to manage and understand the relationships between resources.
A parameters folder is used to store environment-specific parameter files, allowing for easy switching between different configurations (e.g., development, testing, production).

your-project-repo/
│
├── .github/                        # GitHub Actions workflows
│   └── workflows/
│       └── deploy-infrastructure.yml  # Workflow definition for GitHub Actions
│
├── azure-pipelines.yml             # Azure DevOps pipeline definition
│
├── main.bicep                      # Main Bicep file that orchestrates the deployment
│
├── modules/                        # Folder containing all Bicep modules
│   ├── compute/
│   │   └── vm.bicep                # Bicep module for Virtual Machine creation
│   │
│   ├── core/
│   │   └── resourceGroup.bicep     # Bicep module for Resource Group creation
│   │
│   ├── data/
│   │   ├── sqlDatabase.bicep       # Bicep module for Azure SQL Database creation
│   │   └── storageAccount.bicep    # Bicep module for Azure Storage Account creation
│   │
│   └── network/
│       ├── nsg.bicep               # Bicep module for Network Security Group configuration
│       └── vnet.bicep              # Bicep module for Virtual Network and subnets setup
│
└── parameters/                     # Folder for parameter files
    └── dev.parameters.json         # Parameters for development environment deployment

