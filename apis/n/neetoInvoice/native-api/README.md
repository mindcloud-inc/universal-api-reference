# NeetoInvoice: Native API Reference

A consolidated summary of NeetoInvoice's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.neetoinvoice.com/getting-started/introduction
- **API base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`

## Authentication

### API Key

Authenticate NeetoInvoice API requests with the workspace subdomain and X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required · NeetoInvoice API key used in the X-Api-Key header.
- **Workspace Subdomain:** `workspaceSubdomain` · required · Workspace subdomain used to build requests like https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://apidocs.neetoinvoice.com/getting-started/authentication)

## Pagination

Use `page_size` in the query string to set the page size (default 30; accepted range 1–100). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project User](actions/add-project-user.md) | `POST /projects/{project_id}/project_users` | [docs](https://apidocs.neetoinvoice.com/api-reference/project-users/add) |
| [Add Team Members](actions/add-team-members.md) | `POST /team_members` | [docs](https://apidocs.neetoinvoice.com/api-reference/team-members/add) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://apidocs.neetoinvoice.com/api-reference/clients/create) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://apidocs.neetoinvoice.com/api-reference/projects/create) |
| [Create Recipient](actions/create-recipient.md) | `POST /clients/{client_id}/recipients` | [docs](https://apidocs.neetoinvoice.com/api-reference/recipients/create) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /time_entry` | [docs](https://apidocs.neetoinvoice.com/api-reference/time-entry/create) |
| [Delete Recipient](actions/delete-recipient.md) | `DELETE /clients/{client_id}/recipients/{recipient_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/recipients/delete) |
| [Generate Invoice](actions/generate-invoice.md) | `POST /clients/{client_id}/invoices` | [docs](https://apidocs.neetoinvoice.com/api-reference/invoices/create) |
| [Get Client](actions/get-client.md) | `GET /clients/{client_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/clients/get) |
| [Get Project](actions/get-project.md) | `GET /projects/{project_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/projects/get) |
| [List Project Users](actions/list-project-users.md) | `GET /projects/{project_id}/project_users` | [docs](https://apidocs.neetoinvoice.com/api-reference/project-users/list) |
| [List Team Members](actions/list-team-members.md) | `GET /team_members` | [docs](https://apidocs.neetoinvoice.com/api-reference/team-members/list) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time_entries` | [docs](https://apidocs.neetoinvoice.com/api-reference/time-entry/list) |
| [Remove Project User](actions/remove-project-user.md) | `DELETE /projects/{project_id}/project_users/{project_user_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/project-users/remove) |
| [Remove Team Members](actions/remove-team-members.md) | `DELETE /team_members` | [docs](https://apidocs.neetoinvoice.com/api-reference/team-members/remove) |
| [Update Client](actions/update-client.md) | `PUT /clients/{client_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/clients/update) |
| [Update Client Status](actions/update-client-status.md) | `POST /clients/update_status` | [docs](https://apidocs.neetoinvoice.com/api-reference/clients/update-status) |
| [Update Project](actions/update-project.md) | `PATCH /projects/{project_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/projects/update) |
| [Update Project Status](actions/update-project-status.md) | `POST /projects/update_status` | [docs](https://apidocs.neetoinvoice.com/api-reference/projects/update-status) |
| [Update Project User](actions/update-project-user.md) | `PATCH /projects/{project_id}/project_users/{project_user_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/project-users/update) |
| [Update Recipient](actions/update-recipient.md) | `PUT /clients/{client_id}/recipients/{recipient_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/recipients/update) |
| [Update Team Member](actions/update-team-member.md) | `PATCH /team_members/{team_member_id}` | [docs](https://apidocs.neetoinvoice.com/api-reference/team-members/update) |
