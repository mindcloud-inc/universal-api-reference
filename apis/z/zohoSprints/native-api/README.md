# Zoho Sprints: Native API Reference

A consolidated summary of Zoho Sprints's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://sprints.zoho.com/apidoc.html
- **API base URL:** `https://sprintsapi.zoho.com/zsapi`

## Authentication

### OAuth 2.0

Connect Zoho Sprints with Zoho OAuth 2.0 authorization-code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoSprints.teams.READ ZohoSprints.teamusers.READ ZohoSprints.projects.READ ZohoSprints.projects.CREATE ZohoSprints.projects.UPDATE ZohoSprints.sprints.READ ZohoSprints.sprints.CREATE ZohoSprints.sprints.UPDATE ZohoSprints.items.READ ZohoSprints.items.CREATE ZohoSprints.items.UPDATE ZohoSprints.comments.READ ZohoSprints.comments.CREATE ZohoSprints.settings.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://sprints.zoho.com/apidoc.html)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Item Attachments](actions/add-item-attachments.md) | `POST /team/:teamId/projects/:projectId/sprints/:sprintId/item/:itemId/attachments/` | [docs](https://sprints.zoho.com/apidoc.html#Additemattachments) |
| [Complete Sprint](actions/complete-sprint.md) | `POST /team/:teamId/projects/:projectId/sprints/:sprintId/complete/?action=complete` | [docs](https://sprints.zoho.com/apidoc.html#Completesprint) |
| [Create Item](actions/create-item.md) | `POST /team/:teamId/projects/:projectId/sprints/:sprintId/item/` | [docs](https://sprints.zoho.com/apidoc.html#Createitem) |
| [Create Project](actions/create-project.md) | `POST /team/:teamId/projects/` | [docs](https://sprints.zoho.com/apidoc.html#Createproject) |
| [Create Sprint](actions/create-sprint.md) | `POST /team/:teamId/projects/:projectId/sprints/` | [docs](https://sprints.zoho.com/apidoc.html#Createsprint) |
| [Get Item Details](actions/get-item-details.md) | `GET /team/:teamId/projects/:projectId/sprints/:sprintId/item/:itemId/` | [docs](https://sprints.zoho.com/apidoc.html#Getitemdetails) |
| [Get Project Backlog](actions/get-project-backlog.md) | `GET /team/:teamId/projects/:projectId/` | [docs](https://sprints.zoho.com/apidoc.html#Getprojectbacklog) |
| [Get Project Details](actions/get-project-details.md) | `GET /team/:teamId/projects/:projectId/` | [docs](https://sprints.zoho.com/apidoc.html#Getprojectdetails) |
| [Get Project Status](actions/get-project-status.md) | `GET /team/:teamId/projects/:projectId/itemstatus/` | [docs](https://sprints.zoho.com/apidoc.html#Getprojectstatus) |
| [Get Sprint Details](actions/get-sprint-details.md) | `GET /team/:teamId/projects/:projectId/sprints/:sprintId/?action=details` | [docs](https://sprints.zoho.com/apidoc.html#Getsprintdetails) |
| [Get Workspace Settings](actions/get-workspace-settings.md) | `GET /team/:teamId/settings/` | [docs](https://sprints.zoho.com/apidoc.html#Getworkspacesettings) |
| [List Item Types](actions/list-item-types.md) | `GET /team/:teamId/projects/:projectId/itemtype/` | [docs](https://sprints.zoho.com/apidoc.html#Getitemtypes) |
| [List Items](actions/list-items.md) | `GET /team/:teamId/projects/:projectId/sprints/:sprintId/item/` | [docs](https://sprints.zoho.com/apidoc.html#Getitems) |
| [List Project Priorities](actions/list-project-priorities.md) | `GET /team/:teamId/projects/:projectId/priority/` | [docs](https://sprints.zoho.com/apidoc.html#Getprojectpriorities) |
| [List Projects](actions/list-projects.md) | `GET /team/:teamId/projects/` | [docs](https://sprints.zoho.com/apidoc.html#Getprojects) |
| [List Sprints](actions/list-sprints.md) | `GET /team/:teamId/projects/:projectId/sprints/?action=data&index=1&range=50&type={{sprintTypeArr}}&searchvalue={{searchValue}}` | [docs](https://sprints.zoho.com/apidoc.html#Getsprints) |
| [List Tags](actions/list-tags.md) | `GET /team/:teamId/tags/` | [docs](https://sprints.zoho.com/apidoc.html#Gettags) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET /team/:teamId/users/` | [docs](https://sprints.zoho.com/apidoc.html#Getworkspaceusers) |
| [List Workspaces](actions/list-workspaces.md) | `GET /teams/` | [docs](https://sprints.zoho.com/apidoc.html#Getallworkspaces) |
| [Move Item](actions/move-item.md) | `POST /team/:teamId/projects/:projectId/sprints/:sprintId/bulkupdate/` | [docs](https://sprints.zoho.com/apidoc.html#Moveitem) |
| [Start Sprint](actions/start-sprint.md) | `POST /team/:teamId/projects/:projectId/sprints/:sprintId/start/?action=start` | [docs](https://sprints.zoho.com/apidoc.html#Startsprint) |
| [Update Item](actions/update-item.md) | `POST /team/:teamId/projects/:projectId/sprints/:sprintId/item/:itemId/` | [docs](https://sprints.zoho.com/apidoc.html#Updateitem) |
| [Update Project](actions/update-project.md) | `POST /team/:teamId/projects/:projectId/` | [docs](https://sprints.zoho.com/apidoc.html#Updateproject) |
