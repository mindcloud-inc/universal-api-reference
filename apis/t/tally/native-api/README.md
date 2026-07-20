# Tally: Native API Reference

A consolidated summary of Tally's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://developers.tally.so/api-reference/introduction
- **API base URL:** `https://api.tally.so`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.tally.so/api-reference/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Send sorting in the query string. Only one sort field is accepted.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Invite](actions/cancel-invite.md) | `GET organizations/:organizationId/invites/:inviteId` | [docs](https://developers.tally.so/api-reference/endpoint/organizations/invites/delete) |
| [Create Invite](actions/create-invite.md) | `POST organizations/:organizationId/invites` | [docs](https://developers.tally.so/api-reference/endpoint/organizations/invites/post) |
| [Create Workspace](actions/create-workspace.md) | `POST workspaces` | [docs](https://developers.tally.so/api-reference/endpoint/workspaces/post) |
| [Delete Form](actions/delete-form.md) | `DELETE forms/:formId` | [docs](https://developers.tally.so/api-reference/endpoint/forms/delete) |
| [Delete Form Submission](actions/delete-form-submission.md) | `DELETE forms/:formId/submissions/:submissionId` | [docs](https://developers.tally.so/api-reference/endpoint/forms/submissions/delete) |
| [Delete User](actions/delete-user.md) | `DELETE organizations/:organizationId/users/:userId` | [docs](https://developers.tally.so/api-reference/endpoint/organizations/users/delete) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE workspaces/:workspaceId` | [docs](https://developers.tally.so/api-reference/endpoint/workspaces/delete) |
| [Get Form](actions/get-form.md) | `GET forms/:formId` | [docs](https://developers.tally.so/api-reference/endpoint/forms/get) |
| [Get Form Submission](actions/get-form-submission.md) | `GET forms/:formId/submissions/:submissionId` | [docs](https://developers.tally.so/api-reference/endpoint/forms/submissions/get) |
| [Get User Info](actions/get-user-info.md) | `GET https://api.tally.so/users/me` | [docs](https://developers.tally.so/api-reference/endpoint/users/me/get) |
| [Get Workspace](actions/get-workspace.md) | `GET workspaces/:workspaceId` | [docs](https://developers.tally.so/api-reference/endpoint/workspaces/get) |
| [List Form Questions](actions/list-form-questions.md) | `GET forms/:formId/questions` | [docs](https://developers.tally.so/api-reference/endpoint/forms/questions/list) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET forms/:formId/submissions` | [docs](https://developers.tally.so/api-reference/endpoint/forms/submissions/list) |
| [List Forms](actions/list-forms.md) | `GET forms` | [docs](https://developers.tally.so/api-reference/endpoint/forms/list) |
| [List Invites](actions/list-invites.md) | `GET organizations/:organizationId/invites` | [docs](https://developers.tally.so/api-reference/endpoint/organizations/invites/delete) |
| [List Users](actions/list-users.md) | `GET organizations/:organizationId/users` | [docs](https://developers.tally.so/api-reference/endpoint/organizations/users/get) |
| [List Workspaces](actions/list-workspaces.md) | `GET workspaces` | [docs](https://developers.tally.so/api-reference/endpoint/workspaces/list) |
| [Update Workspace](actions/update-workspace.md) | `PATCH workspaces/:workspaceId` | [docs](https://developers.tally.so/api-reference/endpoint/workspaces/patch) |
