# NeetoForm: Native API Reference

A consolidated summary of NeetoForm's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.neetoform.com/getting-started/introduction
- **API base URL:** `https://{workspaceSubdomain}.neetoform.com/api/external/v1`

## Authentication

### API Key

Authenticate with a workspace-specific NeetoForm API key.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace Subdomain:** `workspaceSubdomain` · required · Enter your NeetoForm workspace subdomain only, without .neetoform.com. Do not enter the workspace display name.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.neetoform.com/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 30). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Team Members](actions/add-team-members.md) | `POST /team_members` | [docs](https://apidocs.neetoform.com/api-reference/team-members/add) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://apidocs.neetoform.com/api-reference/forms/list) |
| [List Submissions](actions/list-submissions.md) | `GET /forms/:form_id/submissions` | [docs](https://apidocs.neetoform.com/api-reference/submissions/list) |
| [List Team Members](actions/list-team-members.md) | `GET /team_members` | [docs](https://apidocs.neetoform.com/api-reference/team-members/list) |
| [Remove Team Members](actions/remove-team-members.md) | `DELETE /team_members` | [docs](https://apidocs.neetoform.com/api-reference/team-members/remove) |
| [Update Team Member](actions/update-team-member.md) | `PATCH /team_members/:team_member_id` | [docs](https://apidocs.neetoform.com/api-reference/team-members/update) |
