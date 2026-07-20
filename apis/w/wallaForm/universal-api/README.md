# <img src="https://images.mindcloud.co/apps/icons/favicon-home-walla-my-48x48-1_1777036769225.png" alt="Walla Form logo" width="28" height="28"> Walla Form: Universal API

Access Walla workspaces, forms, columns, and response data through Walla's official response API using HTTP Basic authentication with client ID and API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wallaForm/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://walla.my
- **Vendor API docs:** https://home.walla.my/en/help-center/%EC%9D%91%EB%8B%B5-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Get Column Metadata](actions/get-column-metadata.md) | GET |  |
| [Get Project Columns](actions/get-project-columns.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Check Customer Key Exists](actions/check-customer-key-exists.md) | GET |  |
| [List Customer Keys](actions/list-customer-keys.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Project Responses](actions/download-project-responses.md) | GET |  |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Response by Customer Key](actions/get-response-by-customer-key.md) | GET |  |
| [Get Response by Response Key](actions/get-response-by-response-key.md) | GET |  |
| [Query Responses by Date Range](actions/query-responses-by-date-range.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [Get Workspace Key by Project Key](actions/get-workspace-key-by-project-key.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |

