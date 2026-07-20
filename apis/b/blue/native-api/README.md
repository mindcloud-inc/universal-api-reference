# Blue: Native API Reference

A consolidated summary of Blue's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://blue.cc/api
- **API base URL:** `https://api.blue.cc`

## Authentication

### Personal Access Token

Connect Blue with a personal access token secret plus the required token ID and company ID.

### Credentials

- **API Key:** `apiKey` · required
- **Token ID:** `tokenId` · required · Your Blue Personal Access Token ID from the API settings page.
- **Company ID:** `companyId` · required · Your Blue organisation slug or company ID used in the X-Bloo-Company-ID header.

Send these headers with each API request:

```http
X-Bloo-Token-ID: <tokenId>
X-Bloo-Company-ID: <companyId>
X-Bloo-Token-Secret: <apiKey>
```

[Official authentication documentation](https://blue.cc/api/start-guide/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [Delete Project](actions/delete-project.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [Get Company](actions/get-company.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [Get Current User](actions/get-current-user.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [Get Stats](actions/get-stats.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [Get User](actions/get-user.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Available Subscription Plans](actions/list-available-subscription-plans.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Companies](actions/list-companies.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Company Invoices](actions/list-company-invoices.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Company Users](actions/list-company-users.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Dashboards](actions/list-dashboards.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Links](actions/list-links.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List My Invitations](actions/list-my-invitations.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Notification Options](actions/list-notification-options.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Project Folders](actions/list-project-folders.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Projects](actions/list-projects.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Recent Projects](actions/list-recent-projects.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Reports](actions/list-reports.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [List Webhooks](actions/list-webhooks.md) | `POST /graphql` | [docs](https://blue.cc/api) |
| [Update Project](actions/update-project.md) | `POST /graphql` | [docs](https://blue.cc/api) |
