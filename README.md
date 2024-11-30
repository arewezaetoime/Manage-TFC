# Manage-TFC

This repository contains Terraform code to manage HCP Terraform Cloud resources.

## Prerequisites

Before you begin, ensure you have the following:

1. **Terraform CLI**: Install Terraform CLI (version 1.5.0 or above).
2. **HCP Terraform Account**: Create an organization on [HCP Terraform Cloud](https://app.terraform.io).
3. **Generate your user API token**: 
   - Use the following command to generate a user token:
   ```bash
     terraform login
   ```
   - Save in a save place so you can paste it in _terraform.tfvars_ under `tfe_token` key later on.
4. **GitHub Repository**: Ensure that your GitHub repository exists and is accessible.
5. **GitHub OAuth Token**: Generate a GitHub OAuth token for the `github_oauth_token_id` value in the _terraform.tfvars_ variables definition file. The token should have a repository scope.  
   To generate the GitHub OAuth token:
   - Go to your GitHub [Github -> User -> Settings-> Developer Setting -> Personal Access Tokens - Fine-grained tokens](https://github.com/settings/tokens?type=beta).
   - Save in a save place so you can paste it in _terraform.tfvars_ under `github_oauth_token_id` key later on.


## Setup Instructions

Follow these steps to set up the project:

🟣<span style="color: purple;">1. **Clone the Repository**:</span>
```bash
   git clone https://github.com/arewezaetoime/Manage-TFC.git
   cd Manage-TFC
```

🟣<span style="color: purple;">2.**Create terraform file from the example file and update the variables**:</span>
```bash
- cp terraform.tfvars.example terraform.tfvars
```
- Replace the example `tfe_token` and `github_oauth_token_id` values with your own tokens in the "terraform.tfvars" file and save it.

🟣<span style="color: purple;">3.**Run the shell script for your convenience**:</span>
To simplify the process of initializing, planning, and applying resources, a shell script is provided. Run the script from the working directory as the final step.

Note: Make the script executable with the following command:
```bash
chmod +x setup_hcp_terraform.sh
```
- Execute the script:
```bash
./setup_hcp_terraform.sh
```