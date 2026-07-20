# ByteForms: Native API Reference

A consolidated summary of ByteForms's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://forms.bytesuite.io/docs/api
- **API base URL:** `https://api.forms.bytesuite.io/`

## Authentication

### API Key

Connect ByteForms with your API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://forms.bytesuite.io/docs/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | `POST /api/workspace` | [docs](https://forms.bytesuite.io/docs/api) |
| [Delete Form](actions/delete-form.md) | `DELETE /api/form/:formId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Delete Response](actions/delete-response.md) | `DELETE /api/form/response/:responseId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /api/workspace/:workspaceId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Export Responses CSV](actions/export-responses-csv.md) | `GET /api/form/export/csv/:formId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Export Responses XLSX](actions/export-responses-xlsx.md) | `GET /api/form/export/xlsx/:formId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Active Subscription](actions/get-active-subscription.md) | `GET /api/subscription/active` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Current User](actions/get-current-user.md) | `GET /api/user/me` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Form](actions/get-form.md) | `GET /api/form/:formId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Form Analytics](actions/get-form-analytics.md) | `GET /api/form/analytics/:formId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Form Responses](actions/get-form-responses.md) | `GET /api/form/responses/:formId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Invited Members](actions/get-invited-members.md) | `GET /api/workspace/invited-members/:workspaceId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Public Form](actions/get-public-form.md) | `GET /f/:publicId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Response](actions/get-response.md) | `GET /api/form/response/:responseId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Subscription Limits](actions/get-subscription-limits.md) | `GET /api/subscription/limits` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/workspace/:workspaceId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Get Workspace Members](actions/get-workspace-members.md) | `GET /api/workspace/members/:workspaceId` | [docs](https://forms.bytesuite.io/docs/api) |
| [List Forms](actions/list-forms.md) | `GET /api/form` | [docs](https://forms.bytesuite.io/docs/api) |
| [List Plans](actions/list-plans.md) | `GET /api/plans` | [docs](https://forms.bytesuite.io/docs/api) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /api/subscription` | [docs](https://forms.bytesuite.io/docs/api) |
| [List Workspace Invites](actions/list-workspace-invites.md) | `GET /api/workspace/invites` | [docs](https://forms.bytesuite.io/docs/api) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/workspace` | [docs](https://forms.bytesuite.io/docs/api) |
| [Update Current User](actions/update-current-user.md) | `POST /api/user/me` | [docs](https://forms.bytesuite.io/docs/api) |
| [Update Form](actions/update-form.md) | `POST /api/form/:formId` | [docs](https://forms.bytesuite.io/docs/api) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /api/workspace/:workspaceId` | [docs](https://forms.bytesuite.io/docs/api) |
