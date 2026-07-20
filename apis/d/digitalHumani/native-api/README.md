# Digital Humani: Native API Reference

A consolidated summary of Digital Humani's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.digitalhumani.com/
- **API base URL:** `https://api.digitalhumani.com`

## Authentication

### API Key

Use your Digital Humani production or sandbox API key from the Developer page.

### Credentials

- **API Key:** `apiKey` · required
- **Enterprise ID:** `enterpriseId` · required · Your Digital Humani enterpriseId from the Developer page. Many enterprise and reporting actions use this value.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.digitalhumani.com/#documentationauthentification)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /user/whoami` | [docs](https://docs.digitalhumani.com/#apiuser_whoami) |
| [Get Enterprise](actions/get-enterprise.md) | `GET /enterprise/:id` | [docs](https://docs.digitalhumani.com/#apienterprise_get) |
| [Get Enterprise Total Tree Count](actions/get-enterprise-total-tree-count.md) | `GET /enterprise/:id/treeCount/total` | [docs](https://docs.digitalhumani.com/#apitree_get_enterprise_total_count) |
| [Get Enterprise Tree Count by Date Range](actions/get-enterprise-tree-count-by-date-range.md) | `GET /enterprise/:id/treeCount` | [docs](https://docs.digitalhumani.com/#apitree_get_enterprise_count) |
| [Get Enterprise Tree Count by Month](actions/get-enterprise-tree-count-by-month.md) | `GET /enterprise/:id/treeCount/:month` | [docs](https://docs.digitalhumani.com/#apitree_get_enterprise_month) |
| [Get Project](actions/get-project.md) | `GET /project/:id` | [docs](https://docs.digitalhumani.com/#apiproject_get) |
| [Get Tree Request](actions/get-tree-request.md) | `GET /tree/:uuid` | [docs](https://docs.digitalhumani.com/#apitree_get_request) |
| [Get User Tree Count](actions/get-user-tree-count.md) | `GET /tree` | [docs](https://docs.digitalhumani.com/#apitree_get_user) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://docs.digitalhumani.com/#apiprojects_list) |
| [Plant Trees](actions/plant-trees.md) | `POST /tree` | [docs](https://docs.digitalhumani.com/#apitree_plant) |
