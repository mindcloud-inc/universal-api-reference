# Zoho Projects: Native API Reference

A consolidated summary of Zoho Projects's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://projectsapi.zoho.com/api-docs
- **API base URL:** `https://projectsapi.zoho.com/api/v3`

## Authentication

### OAuth 2.0

Connect Zoho Projects with Zoho OAuth 2.0 authorization-code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoProjects.portals.READ,ZohoProjects.projects.CREATE,ZohoProjects.projects.READ,ZohoProjects.projects.UPDATE,ZohoProjects.tasklists.CREATE,ZohoProjects.tasklists.READ,ZohoProjects.tasklists.UPDATE,ZohoProjects.tasklists.DELETE,ZohoProjects.tasks.CREATE,ZohoProjects.tasks.READ,ZohoProjects.tasks.UPDATE,ZohoProjects.tasks.DELETE,ZohoProjects.bugs.CREATE,ZohoProjects.bugs.READ,ZohoProjects.bugs.UPDATE,ZohoProjects.bugs.DELETE,ZohoProjects.users.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://projectsapi.zoho.com/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | `POST /portal/[:PORTALID]/projects/[:PROJECTID]/issues` | [docs](https://projectsapi.zoho.com/api-docs#issues_create-an-issue) |
| [Create Project](actions/create-project.md) | `POST /portal/[:PORTALID]/projects` | [docs](https://projectsapi.zoho.com/api-docs#projects_create-a-project) |
| [Create Task](actions/create-task.md) | `POST /portal/[:PORTALID]/projects/[:PROJECTID]/tasks` | [docs](https://projectsapi.zoho.com/api-docs#tasks_create-a-task) |
| [Create Task List](actions/create-task-list.md) | `POST /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists` | [docs](https://projectsapi.zoho.com/api-docs#task-lists_create-task-list) |
| [Delete Issue](actions/delete-issue.md) | `DELETE /portal/[:PORTALID]/projects/[:PROJECTID]/issues/[:ISSUEID]` | [docs](https://projectsapi.zoho.com/api-docs#issues_delete-an-issue) |
| [Delete Task](actions/delete-task.md) | `DELETE /portal/[:PORTALID]/projects/[:PROJECTID]/tasks/[:TASKID]` | [docs](https://projectsapi.zoho.com/api-docs#tasks_delete-a-task) |
| [Delete Task List](actions/delete-task-list.md) | `DELETE /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]` | [docs](https://projectsapi.zoho.com/api-docs#task-lists_delete-task-list) |
| [Get Issue Details](actions/get-issue-details.md) | `GET /portal/[:PORTALID]/projects/[:PROJECTID]/issues/[:ISSUEID]` | [docs](https://projectsapi.zoho.com/api-docs#issues_get-issue-details) |
| [Get Portal Details](actions/get-portal-details.md) | `GET /portal/[:PORTALID]` | [docs](https://projectsapi.zoho.com/api-docs#portals_get-portal-details) |
| [Get Project Details](actions/get-project-details.md) | `GET /portal/[:PORTALID]/projects/[:PROJECTID]` | [docs](https://projectsapi.zoho.com/api-docs#projects_get-project-details) |
| [Get Task Details](actions/get-task-details.md) | `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasks/[:TASKID]` | [docs](https://projectsapi.zoho.com/api-docs#tasks_get-task-details) |
| [Get Task List Details](actions/get-task-list-details.md) | `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]` | [docs](https://projectsapi.zoho.com/api-docs#task-lists_get-task-list-details) |
| [Get User Details](actions/get-user-details.md) | `GET /portal/[:PORTALID]/users/[:USERREF]` | [docs](https://projectsapi.zoho.com/api-docs#users_get-user-details) |
| [List Portal Users, Client Users, And Contacts](actions/list-portal-users-client-users-and-contacts.md) | `GET /portal/[:PORTALID]/users` | [docs](https://projectsapi.zoho.com/api-docs#users_get-all-portal-users-client-users-and-contacts) |
| [List Portals](actions/list-portals.md) | `GET /portals` | [docs](https://projectsapi.zoho.com/api-docs#portals_get-all-portals) |
| [List Project Issues](actions/list-project-issues.md) | `GET /portal/[:PORTALID]/projects/[:PROJECTID]/issues` | [docs](https://projectsapi.zoho.com/api-docs#issues_get-project-issues) |
| [List Project Task Lists](actions/list-project-task-lists.md) | `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists` | [docs](https://projectsapi.zoho.com/api-docs#task-lists_get-all-project-task-lists) |
| [List Projects](actions/list-projects.md) | `GET /portal/[:PORTALID]/projects` | [docs](https://projectsapi.zoho.com/api-docs#projects_get-all-projects) |
| [List Tasks By Project](actions/list-tasks-by-project.md) | `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasks` | [docs](https://projectsapi.zoho.com/api-docs#tasks_get-tasks-by-project) |
| [Trash Project](actions/trash-project.md) | `POST /portal/[:PORTALID]/projects/[:PROJECTID]/trash` | [docs](https://projectsapi.zoho.com/api-docs#projects_trash-a-project) |
| [Update Issue](actions/update-issue.md) | `PATCH /portal/[:PORTALID]/projects/[:PROJECTID]/issues/[:ISSUEID]` | [docs](https://projectsapi.zoho.com/api-docs#issues_update-an-issue) |
| [Update Project](actions/update-project.md) | `PATCH /portal/[:PORTALID]/projects/[:PROJECTID]` | [docs](https://projectsapi.zoho.com/api-docs#projects_update-a-project) |
| [Update Task](actions/update-task.md) | `PATCH /portal/[:PORTALID]/projects/[:PROJECTID]/tasks/[:TASKID]` | [docs](https://projectsapi.zoho.com/api-docs#tasks_update-a-task) |
| [Update Task List](actions/update-task-list.md) | `PATCH /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]` | [docs](https://projectsapi.zoho.com/api-docs#task-lists_update-task-list) |
