terraform-project/
├── modules/                     # Reusable modules for organizing code 
│   ├── network/                 # Example module: networking setup
│   │   ├── main.tf              # Module resources and logic (Provider Configuration, Resource Definitions, Variables, Outputs)
│   │   ├── variables.tf         # Input variables for the module
│   │   ├── outputs.tf           # Output variables for the module
│   │   └── README.md            # Documentation for the module




Commands:

1. terraform state list
Use Case: Check the resources being tracked in your infrastructure.

2. terraform state show [RESOURCE]
Displays detailed information about a specific resource in the state file.
Example: terraform state show aws_instance.my_instance


3. terraform state rm [RESOURCE]
Removes a specific resource from the Terraform state file without deleting it in the cloud.
Use Case: When a resource is managed outside of Terraform.
Example: terraform state rm aws_instance.my_instance



4. terraform workspace list
Lists all available workspaces in the current backend.
Use Case: Managing environments like dev, staging, and prod.


5. terraform workspace new [WORKSPACE_NAME]
Creates a new workspace.
Use Case: Isolating state for different environments.
Example: terraform workspace new staging

6. terraform workspace select [WORKSPACE_NAME]
Switches to a different workspace.
Example: terraform workspace select prod

7. terraform workspace delete [WORKSPACE_NAME]
Deletes an unused workspace.
Use Case: Cleaning up unused environments.


8. terraform import [RESOURCE_NAME] [ID]
Imports existing infrastructure into Terraform state.
Use Case: Managing resources that were created outside of Terraform.


9. terraform providers
Use Case: Checking dependencies and versions.



------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Terraform Resource Definition and Resource Identifier
Terraform uses resource definitions to declare the infrastructure you want to manage and resource identifiers to reference and interact with specific resources within and outside Terraform.

Eg: resource "<provider>_<type>" "<name>" {
  <key> = <value>
  ...
}









