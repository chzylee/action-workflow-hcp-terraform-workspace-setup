# action-workflow-hcp-terraform-workspace

## Usage

Use this action in a GitHub Action pipeline to create/update an HCP Terraform workspace. Follow the example below to see how to use this action in a GitHub Action.

### Example

In your repository, create a workflow file (e.g., `.github/workflows/deploy.yml`) with the following content:

```yaml
name: Setup Workspace

on:
  workflow_dispatch:

jobs:
  deploy:
    uses: chzylee/action-workflow-hcp-terraform-run@v1.1.1
    with:
      tfc_hostname: 'app.terraform.io'
      tfc_organization: 'your-tfc-org'
      tfc_workspace: 'your-workspace'
      tfc_project: 'project-id'
      tfc_token: ${{ secrets.TF_API_TOKEN }}
```

### Inputs

| Name             | Description                       | Required | Example            |
| ---------------- | --------------------------------- | -------- | ------------------ |
| tfc_hostname     | Terraform Cloud hostname          | Yes      | `app.terraform.io` |
| tfc_organization | Terraform Cloud organization name | Yes      | `my-org`           |
| tfc_workspace    | Terraform Cloud workspace name    | Yes      | `my-workspace`     |
| tfc_project      | Terraform Cloud workspace name    | Yes      | `prj-abcd`         |
| tfc_token        | Terraform Cloud workspace name    | Yes      | `my-workspace`     |

---
