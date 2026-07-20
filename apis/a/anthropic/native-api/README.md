# Anthropic: Native API Reference

A consolidated summary of Anthropic's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://platform.claude.com/docs/en/api/overview
- **API base URL:** `https://api.anthropic.com`

## Authentication

### API Key

Authenticate using Anthropic API keys via the x-api-key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.anthropic.com/en/api/overview)

## API conventions

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `last_id`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–1000). Use `after_id` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Message Batch](actions/cancel-message-batch.md) | `POST /v1/messages/batches/:message_batch_id/cancel` | [docs](https://platform.claude.com/docs/en/api/messages/batches/cancel) |
| [Count Message Tokens](actions/count-message-tokens.md) | `POST /v1/messages/count_tokens` | [docs](https://platform.claude.com/docs/en/api/messages/count_tokens) |
| [Create Invite](actions/create-invite.md) | `POST /v1/organizations/invites` | [docs](https://platform.claude.com/docs/en/api/admin/invites/create) |
| [Create Message](actions/create-message.md) | `POST /v1/messages` | [docs](https://platform.claude.com/docs/en/api/messages/create) |
| [Create Message Batch](actions/create-message-batch.md) | `POST /v1/messages/batches` | [docs](https://platform.claude.com/docs/en/api/messages/batches/create) |
| [Create Skill](actions/create-skill.md) | `POST /v1/skills` | [docs](https://platform.claude.com/docs/en/api/beta/skills/create) |
| [Create Workspace](actions/create-workspace.md) | `POST /v1/organizations/workspaces` | [docs](https://platform.claude.com/docs/en/api/admin/workspaces/create) |
| [Create Workspace Member](actions/create-workspace-member.md) | `POST /v1/organizations/workspaces/{workspace_id}/members` | [docs](https://platform.claude.com/docs/en/api/admin/workspaces/members/create) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/files/:file_id` | [docs](https://platform.claude.com/docs/en/api/beta/files/delete) |
| [Delete Invite](actions/delete-invite.md) | `DELETE /v1/organizations/invites/{invite_id}` | [docs](https://platform.claude.com/docs/en/api/admin/invites/delete) |
| [Delete Message Batch](actions/delete-message-batch.md) | `DELETE /v1/messages/batches/:message_batch_id` | [docs](https://platform.claude.com/docs/en/api/messages/batches/delete) |
| [Delete Skill](actions/delete-skill.md) | `DELETE /v1/skills/:skill_id` | [docs](https://platform.claude.com/docs/en/api/beta/skills/delete) |
| [Download File](actions/download-file.md) | `GET /v1/files/:file_id/content` | [docs](https://platform.claude.com/docs/en/api/beta/files/download) |
| [Get Cost Report](actions/get-cost-report.md) | `GET /v1/organizations/cost_report` | [docs](https://platform.claude.com/docs/en/api/admin/cost_report/retrieve) |
| [Get Current Organization](actions/get-current-organization.md) | `GET /v1/organizations/me` | [docs](https://platform.claude.com/docs/en/api/admin/organizations/me) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /v1/files/:file_id` | [docs](https://platform.claude.com/docs/en/api/beta/files/retrieve_metadata) |
| [Get Messages Usage Report](actions/get-messages-usage-report.md) | `GET /v1/organizations/usage_report/messages` | [docs](https://platform.claude.com/docs/en/api/admin/usage_report/retrieve_messages) |
| [Get Model](actions/get-model.md) | `GET /v1/models/:model_id` | [docs](https://platform.claude.com/docs/en/api/models/retrieve) |
| [Get Skill](actions/get-skill.md) | `GET /v1/skills/:skill_id` | [docs](https://platform.claude.com/docs/en/api/beta/skills/retrieve) |
| [List Files](actions/list-files.md) | `GET /v1/files` | [docs](https://platform.claude.com/docs/en/api/beta/files/list) |
| [List Invites](actions/list-invites.md) | `GET /v1/organizations/invites` | [docs](https://platform.claude.com/docs/en/api/admin/invites/list) |
| [List Message Batches](actions/list-message-batches.md) | `GET /v1/messages/batches` | [docs](https://platform.claude.com/docs/en/api/messages/batches/list) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://platform.claude.com/docs/en/api/models/list) |
| [List Skill Versions](actions/list-skill-versions.md) | `GET /v1/skills/:skill_id/versions` | [docs](https://platform.claude.com/docs/en/api/beta/skills/versions/list) |
| [List Skills](actions/list-skills.md) | `GET /v1/skills` | [docs](https://platform.claude.com/docs/en/api/beta/skills/list) |
| [List Users](actions/list-users.md) | `GET /v1/organizations/users` | [docs](https://platform.claude.com/docs/en/api/admin/users/list) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/organizations/workspaces` | [docs](https://platform.claude.com/docs/en/api/admin/workspaces/list) |
| [Retrieve Message Batch](actions/retrieve-message-batch.md) | `GET /v1/messages/batches/:message_batch_id` | [docs](https://platform.claude.com/docs/en/api/messages/batches/retrieve) |
| [Retrieve Message Batch Results](actions/retrieve-message-batch-results.md) | `GET /v1/messages/batches/:message_batch_id/results` | [docs](https://platform.claude.com/docs/en/api/messages/batches/results) |
| [Upload File](actions/upload-file.md) | `POST /v1/files` | [docs](https://platform.claude.com/docs/en/api/beta/files/upload) |
