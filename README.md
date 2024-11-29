# Manage-TFC

This repository contains Terraform code to manage HCP Terraform Cloud resources.

## Prerequisites

Before you begin, ensure you have the following:

1. **Terraform CLI**: Install Terraform CLI (version 1.5.0 or above).
2. **HCP Terraform Account**: Create an organization on [HCP Terraform Cloud](https://app.terraform.io).
3. **GitHub OAuth Token**: Generate a GitHub OAuth token for the `github_oauth_token_id` value in the `terraform.tfvars` variables definition file. The token should have the `repo` scope.  
   To generate the GitHub OAuth token:
   - Go to your GitHub settings (click the circle with your profile picture in the top-right corner).
   - Navigate to **Settings** > **Developer settings** > **Personal access tokens** > **Fine-grained tokens**.
   - Create a new token and adjust the settings and scope as needed, selecting the appropriate permissions.
4. **GitHub Repository**: Ensure that your GitHub repository exists and is accessible.

## Setup Instructions

Follow these steps to set up the project:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/arewezaetoime/Manage-TFC.git
   cd Manage-TFC

2.**Create terraform file from the example file and update the variables**:
- cp terraform.tfvars.example terraform.tfvars
- Replace the example `tfe_token` and `github_oauth_token_id` values with your own tokens in the "terraform.tfvars" file and save it.

3.**Run the shell script for your convenience**:
To simplify the process of initializing, planning, and applying resources, a shell script is provided. Run the script from the working directory as the final step.
./setup_hcp_terraform.sh

Note: Make the script executable with the following command:
chmod +x setup_hcp_terraform.sh