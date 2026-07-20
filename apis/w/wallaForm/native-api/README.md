# Walla Form: Native API Reference

A consolidated summary of Walla Form's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://home.walla.my/en/help-center/%EC%9D%91%EB%8B%B5-api
- **OpenAPI specification:** https://walla-api.data-lab.workers.dev/doc
- **API base URL:** `https://walla-api.data-lab.workers.dev`

## Authentication

### Basic Auth

Authenticate with Walla using HTTP Basic auth. Use your Walla client ID as the username and your Walla API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://home.walla.my/en/help-center/%EC%9D%91%EB%8B%B5-api)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Customer Key Exists](actions/check-customer-key-exists.md) | `GET /workspace/:workspaceKey/project/:projectKey/response/check/customerKey/:customerKey` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Download Project Responses](actions/download-project-responses.md) | `GET /workspace/:workspaceKey/project/:projectKey/response/list` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Get Column Metadata](actions/get-column-metadata.md) | `GET /workspace/:workspaceKey/project/:projectKey/response/list/:columnKey` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Get Project](actions/get-project.md) | `GET /workspace/:workspaceKey/project/:projectKey` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Get Project Columns](actions/get-project-columns.md) | `GET /workspace/:workspaceKey/project/:projectKey/columns` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Get Response by Customer Key](actions/get-response-by-customer-key.md) | `GET /workspace/:workspaceKey/project/:projectKey/response/get/customerKey/:customerKey` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Get Response by Response Key](actions/get-response-by-response-key.md) | `GET /workspace/:workspaceKey/project/:projectKey/response/get/responseKey/:responseKey` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspace/:workspaceKey` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Get Workspace Key by Project Key](actions/get-workspace-key-by-project-key.md) | `GET /workspace/query/projectKey` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [List Customer Keys](actions/list-customer-keys.md) | `GET /workspace/:workspaceKey/project/:projectKey/response/listCustomerKeys` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [List Projects](actions/list-projects.md) | `GET /workspace/:workspaceKey/project/list` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspace/list` | [docs](https://walla-api.data-lab.workers.dev/ui) |
| [Query Responses by Date Range](actions/query-responses-by-date-range.md) | `GET /workspace/:workspaceKey/project/:projectKey/response/query/dateRange` | [docs](https://walla-api.data-lab.workers.dev/ui) |
