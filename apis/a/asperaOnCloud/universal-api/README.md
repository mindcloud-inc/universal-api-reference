# <img src="https://images.mindcloud.co/apps/icons/aspera_1776367875229.jpeg" alt="Aspera on Cloud logo" width="28" height="28"> Aspera on Cloud: Universal API

REST API for IBM Aspera on Cloud files, packages, workspaces, users, and admin resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/asperaOnCloud/latest
- **Category:** Content & Files / Storage
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ibm.com/cloud/aspera
- **Vendor API docs:** https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/Introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Packages](actions/get-packages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-packages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Client Access Key

| Action | Method | Description |
| --- | --- | --- |
| [List Client Access Keys](actions/get-client-access-keys.md) | GET | Retrieves client access keys from Aspera on Cloud. |

### Dropbox Membership

| Action | Method | Description |
| --- | --- | --- |
| [List Dropbox Members](actions/get-dropbox-memberships.md) | GET | Retrieves shared inbox members from Aspera on Cloud. |

### Node

| Action | Method | Description |
| --- | --- | --- |
| [Get Node](actions/get-node-by-id.md) | GET | Retrieves a node from Aspera on Cloud. |
| [List Nodes](actions/get-nodes.md) | GET | Retrieves nodes from Aspera on Cloud. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Create Package](actions/add-package.md) | POST | Creates a new package in Aspera on Cloud. |
| [Delete Package](actions/delete-package.md) | DELETE | Deletes a package from Aspera on Cloud. |
| [Get Package](actions/get-package-by-id.md) | GET | Retrieves a package from Aspera on Cloud. |
| [List Packages](actions/get-packages.md) | GET | Retrieves packages from Aspera on Cloud. |
| [Update Package](actions/update-package.md) | PUT | Updates a package in Aspera on Cloud. |

### Shared Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Shared Inbox](actions/add-dropbox.md) | POST | Creates a new shared inbox in Aspera on Cloud. |
| [Get Shared Inbox](actions/get-dropbox-by-id.md) | GET | Retrieves a shared inbox from Aspera on Cloud. |
| [List Shared Inboxes](actions/get-dropboxes.md) | GET | Retrieves shared inboxes from Aspera on Cloud. |

### Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [List Usage Reports](actions/get-usage-reports.md) | GET | Retrieves usage reports from Aspera on Cloud. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/add-user.md) | POST | Creates a new user in Aspera on Cloud. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Aspera on Cloud. |
| [Get User](actions/get-user-by-id.md) | GET | Retrieves a user from Aspera on Cloud. |
| [List Users](actions/get-users.md) | GET | Retrieves users from Aspera on Cloud. |
| [Update User](actions/update-user.md) | PUT | Updates a user in Aspera on Cloud. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/add-workspace.md) | POST | Creates a new workspace in Aspera on Cloud. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes a workspace from Aspera on Cloud. |
| [Get Workspace](actions/get-workspace-by-id.md) | GET | Retrieves a workspace from Aspera on Cloud. |
| [List Workspaces](actions/get-workspaces.md) | GET | Retrieves workspaces from Aspera on Cloud. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates a workspace in Aspera on Cloud. |

### Workspace Membership

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Members](actions/get-workspace-memberships.md) | GET | Retrieves workspace members from Aspera on Cloud. |

