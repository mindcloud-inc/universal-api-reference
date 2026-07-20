# Aspera on Cloud: Native API Reference

A consolidated summary of Aspera on Cloud's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/Introduction
- **OpenAPI specification:** https://developer.ibm.com/rest/api-hub-catalog/hub/products/PRODUCT--aspera--aspera-on-cloud-api--1.0.18/apis/API--aspera--files-api/content/files-api_0.2.9.json
- **API base URL:** `https://api.ibmaspera.com/api`

## Authentication

### JWT Bearer (OAuth2)

Aspera on Cloud OAuth2 JWT bearer token exchange.

### Credentials

- **Client ID:** `clientId` · required · Aspera API client ID.
- **API User Email:** `userEmail` · required · Email address used as the JWT subject claim.
- **Scope:** `scope` · required · Requested Aspera API scope, typically user:all.
- **Tenant URL:** `tenantUrl` · optional · Optional Aspera tenant URL used to derive the organization-specific token endpoint.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/AoC+API+authentication+set+up)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Shared Inbox](actions/add-dropbox.md) | `POST /v1/dropboxes` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#add_dropbox) |
| [Create Package](actions/add-package.md) | `POST /v1/packages` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#add_package) |
| [Create User](actions/add-user.md) | `POST /v1/users` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#add_user) |
| [Create Workspace](actions/add-workspace.md) | `POST /v1/workspaces` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#add_workspace) |
| [Delete Package](actions/delete-package.md) | `DELETE /v1/packages/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#delete_package) |
| [Delete User](actions/delete-user.md) | `DELETE /v1/users/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#delete_user) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /v1/workspaces/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#delete_workspace) |
| [List Client Access Keys](actions/get-client-access-keys.md) | `GET /v1/client_access_keys` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_client_access_keys) |
| [Get Shared Inbox](actions/get-dropbox-by-id.md) | `GET /v1/dropboxes/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_dropbox_by_id) |
| [List Dropbox Members](actions/get-dropbox-memberships.md) | `GET /v1/dropbox_memberships` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_dropbox_memberships) |
| [List Shared Inboxes](actions/get-dropboxes.md) | `GET /v1/dropboxes` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_dropboxes) |
| [Get Node](actions/get-node-by-id.md) | `GET /v1/nodes/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_node_by_id) |
| [List Nodes](actions/get-nodes.md) | `GET /v1/nodes` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_nodes) |
| [Get Package](actions/get-package-by-id.md) | `GET /v1/packages/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_package_by_id) |
| [List Packages](actions/get-packages.md) | `GET /v1/packages` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_packages) |
| [List Usage Reports](actions/get-usage-reports.md) | `GET /v1/usage_reports` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_usage_reports) |
| [Get User](actions/get-user-by-id.md) | `GET /v1/users/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_user_by_id) |
| [List Users](actions/get-users.md) | `GET /v1/users` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_users) |
| [Get Workspace](actions/get-workspace-by-id.md) | `GET /v1/workspaces/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_workspace_by_id) |
| [List Workspace Members](actions/get-workspace-memberships.md) | `GET /v1/workspace_memberships` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_workspace_memberships) |
| [List Workspaces](actions/get-workspaces.md) | `GET /v1/workspaces` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#get_workspaces) |
| [Update Package](actions/update-package.md) | `PUT /v1/packages/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#update_package) |
| [Update User](actions/update-user.md) | `PUT /v1/users/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#update_user) |
| [Update Workspace](actions/update-workspace.md) | `PUT /v1/workspaces/{id}` | [docs](https://developer.ibm.com/apis/catalog/aspera--aspera-on-cloud-api/api/API--aspera--files-api#update_workspace) |
