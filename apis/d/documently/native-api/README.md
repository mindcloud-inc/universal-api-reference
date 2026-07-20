# Documently: Native API Reference

A consolidated summary of Documently's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://app.documently.io/api/docs
- **OpenAPI specification:** https://app.documently.io/api/docs.jsonld
- **API base URL:** `https://app.documently.io/api`

## Authentication

### Access Token

Use a Documently access token obtained from the non-OAuth login flow.

### Credentials

- **Access Token:** `accessToken` · required · Documently bearer token used in the Authorization header after sign-in.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://documently.io/documentation/overview)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Branch](actions/create-branch.md) | `POST /branches` | [docs](https://app.documently.io/api/docs) |
| [Create Invitation](actions/create-invitation.md) | `POST /invitations` | [docs](https://app.documently.io/api/docs) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://app.documently.io/api/docs) |
| [Delete Branch](actions/delete-branch.md) | `DELETE /branches/:branchId` | [docs](https://app.documently.io/api/docs) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://app.documently.io/api/docs) |
| [List API Tokens](actions/list-api-tokens.md) | `GET /api-tokens` | [docs](https://app.documently.io/api/docs) |
| [List Articles](actions/list-articles.md) | `GET /articles` | [docs](https://app.documently.io/api/docs) |
| [List Branches](actions/list-branches.md) | `GET /branches` | [docs](https://app.documently.io/api/docs) |
| [List Invitations](actions/list-invitations.md) | `GET /invitations` | [docs](https://app.documently.io/api/docs) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://app.documently.io/api/docs) |
| [List Permissions](actions/list-permissions.md) | `GET /permissions` | [docs](https://app.documently.io/api/docs) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://app.documently.io/api/docs) |
| [List Storage Directories](actions/list-storage-directories.md) | `GET /storage-directories` | [docs](https://app.documently.io/api/docs) |
| [List Storage Files](actions/list-storage-files.md) | `GET /storage` | [docs](https://app.documently.io/api/docs) |
| [List Webhook Logs](actions/list-webhook-logs.md) | `GET /webhook-logs` | [docs](https://app.documently.io/api/docs) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Branch](actions/retrieve-branch.md) | `GET /branches/:branchId` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Current User](actions/retrieve-current-user.md) | `GET /users/me` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Invitation](actions/retrieve-invitation.md) | `GET /invitations/:invitationId` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Organization](actions/retrieve-organization.md) | `GET /organizations/:organizationId` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Permission](actions/retrieve-permission.md) | `GET /permissions/:permissionId` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /projects/:projectId` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Storage Directory](actions/retrieve-storage-directory.md) | `GET /storage-directories/:directoryId` | [docs](https://app.documently.io/api/docs) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:userId` | [docs](https://app.documently.io/api/docs) |
| [Retrieve Webhook](actions/retrieve-webhook.md) | `GET /webhooks/:webhookId` | [docs](https://app.documently.io/api/docs) |
| [Update Branch](actions/update-branch.md) | `PATCH /branches/:branchId` | [docs](https://app.documently.io/api/docs) |
| [Update Permission](actions/update-permission.md) | `PATCH /permissions/:permissionId` | [docs](https://app.documently.io/api/docs) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:projectId` | [docs](https://app.documently.io/api/docs) |
| [Update Storage Directory](actions/update-storage-directory.md) | `PATCH /storage-directories/:directoryId` | [docs](https://app.documently.io/api/docs) |
| [Update User](actions/update-user.md) | `PATCH /users/:userId` | [docs](https://app.documently.io/api/docs) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:webhookId` | [docs](https://app.documently.io/api/docs) |
