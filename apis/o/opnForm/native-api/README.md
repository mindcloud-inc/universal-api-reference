# OpnForm: Native API Reference

A consolidated summary of OpnForm's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.opnform.com/api-reference/introduction
- **OpenAPI specification:** https://docs.opnform.com/api-reference/openapi.yaml
- **API base URL:** `https://api.opnform.com`

## Authentication

### Personal Access Token

Use a Personal Access Token created in OpnForm Settings -> Access Tokens. Required abilities for this app build: workspaces-read, workspaces-write, forms-read, forms-write, workspace-users-read, workspace-users-write, and manage-integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.opnform.com/api-reference/api-keys)

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
| [Add Workspace User](actions/add-workspace-user.md) | `POST /open/workspaces/:workspaceId/users/add` | [docs](https://docs.opnform.com/api-reference/workspace-users/add-workspace-user) |
| [Cancel Workspace Invite](actions/cancel-workspace-invite.md) | `DELETE /open/workspaces/:workspaceId/invites/:inviteId/cancel` | [docs](https://docs.opnform.com/api-reference/workspace-users/cancel-workspace-invite) |
| [Check Submission Export Status](actions/check-submission-export-status.md) | `GET /open/forms/:id/submissions/export/status/:jobId` | [docs](https://docs.opnform.com/api-reference/submissions/export-status) |
| [Create Form](actions/create-form.md) | `POST /open/forms` | [docs](https://docs.opnform.com/api-reference/forms/create-form) |
| [Create Webhook Integration](actions/create-webhook-integration.md) | `POST /open/forms/:formId/integrations` | [docs](https://docs.opnform.com/api-reference/integrations/create-webhook-integration) |
| [Create Workspace](actions/create-workspace.md) | `POST /open/workspaces/create` | [docs](https://docs.opnform.com/api-reference/workspaces/create-workspace) |
| [Delete Form](actions/delete-form.md) | `DELETE /open/forms/:id` | [docs](https://docs.opnform.com/api-reference/forms/delete-form) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /open/forms/:id/submissions/:submissionId` | [docs](https://docs.opnform.com/api-reference/submissions/delete-submission) |
| [Delete Webhook Integration](actions/delete-webhook-integration.md) | `DELETE /open/forms/:formId/integrations/:integrationId` | [docs](https://docs.opnform.com/api-reference/integrations/delete-webhook-integration) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /open/workspaces/:workspaceId` | [docs](https://docs.opnform.com/api-reference/workspaces/delete-workspace) |
| [Export Submissions CSV](actions/export-submissions-csv.md) | `POST /open/forms/:id/submissions/export` | [docs](https://docs.opnform.com/api-reference/submissions/export-submissions-csv) |
| [Get Form](actions/get-form.md) | `GET /open/forms/:slug` | [docs](https://docs.opnform.com/api-reference/forms/get-form) |
| [List Form Integrations](actions/list-form-integrations.md) | `GET /open/forms/:formId/integrations` | [docs](https://docs.opnform.com/api-reference/integrations/list-form-integrations) |
| [List Submissions](actions/list-submissions.md) | `GET /open/forms/:id/submissions` | [docs](https://docs.opnform.com/api-reference/submissions/list-submissions) |
| [List Workspace Forms](actions/list-workspace-forms.md) | `GET /open/workspaces/:workspaceId/forms` | [docs](https://docs.opnform.com/api-reference/forms/list-workspace-forms) |
| [List Workspace Invites](actions/list-workspace-invites.md) | `GET /open/workspaces/:workspaceId/invites` | [docs](https://docs.opnform.com/api-reference/workspace-users/list-workspace-invites) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET /open/workspaces/:workspaceId/users` | [docs](https://docs.opnform.com/api-reference/workspace-users/list-workspace-users) |
| [List Workspaces](actions/list-workspaces.md) | `GET /open/workspaces` | [docs](https://docs.opnform.com/api-reference/workspaces/list-workspaces) |
| [Remove Workspace User](actions/remove-workspace-user.md) | `DELETE /open/workspaces/:workspaceId/users/:userId/remove` | [docs](https://docs.opnform.com/api-reference/workspace-users/remove-workspace-user) |
| [Update Form](actions/update-form.md) | `PUT /open/forms/:id` | [docs](https://docs.opnform.com/api-reference/forms/update-form) |
| [Update Submission](actions/update-submission.md) | `PUT /open/forms/:id/submissions/:submissionId` | [docs](https://docs.opnform.com/api-reference/submissions/update-submission) |
| [Update Webhook Integration](actions/update-webhook-integration.md) | `PUT /open/forms/:formId/integrations/:integrationId` | [docs](https://docs.opnform.com/api-reference/integrations/update-webhook-integration) |
| [Update Workspace](actions/update-workspace.md) | `PUT /open/workspaces/:workspaceId` | [docs](https://docs.opnform.com/api-reference/workspaces/update-workspace) |
| [Update Workspace User Role](actions/update-workspace-user-role.md) | `PUT /open/workspaces/:workspaceId/users/:userId/update-role` | [docs](https://docs.opnform.com/api-reference/workspace-users/update-workspace-user-role) |
