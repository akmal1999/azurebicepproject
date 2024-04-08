# azureproject
This project is built based 
"Evaluation Project: Bicep
Objective
Establish a secure and scalable Azure environment tailored for a web application hosted on a Virtual Machine (VM), ensuring high availability, automated deployment, security, and monitoring. The setup must use Bicep for infrastructure definition and include both an Azure SQL Database and a Storage Account, with configurations and deployment processes documented and pushed to a public GitHub repository."

Project Info.

This project is modularized for future expansion and to templatize and organize for future usage.
The modules folder contains subfolders for each logical grouping of resources (like network, compute, data, and core). This makes it easier to manage and understand the relationships between resources.
A parameters folder is used to store environment-specific parameter files, allowing for easy switching between different configurations (e.g., development, testing, production).

my-project/
│
├── main.bicep
├── resourceGroup.bicep
├── network.bicep
├── vm.bicep
├── sqlDatabase.bicep
├── storageAccount.bicep
└── nsg.bicep


my-project/
│
├── main.bicep             // Orchestration file that references modules
│
├── modules/               // Folder containing all modules
│   ├── network/
│   │   ├── vnet.bicep
│   │   └── nsg.bicep
│   │
│   ├── compute/
│   │   └── vm.bicep
│   │
│   ├── data/
│   │   ├── sqlDatabase.bicep
│   │   └── storageAccount.bicep
│   │
│   └── core/
│       └── resourceGroup.bicep
│
└── parameters/            // (Optional) Folder for parameter files if needed
    └── dev.parameters.json
