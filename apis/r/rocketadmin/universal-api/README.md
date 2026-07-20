# <img src="https://images.mindcloud.co/apps/icons/rocketadmin_1774990306728.png" alt="Rocketadmin logo" width="28" height="28"> Rocketadmin: Universal API

Rocketadmin is an AI-powered admin panel for databases with REST API access for users, connections, tables, rows, filters, logs, and saved queries.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rocketadmin/latest
- **Category:** IT Operations / Database
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rocketadmin.com
- **Vendor API docs:** https://docs.rocketadmin.com/api-reference/rocketadmin

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Key](actions/check-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | GET |  |
| [Create API Key](actions/create-api-key.md) | POST |  |
| [Delete API Key](actions/delete-api-key.md) | DELETE |  |
| [Get API Key](actions/get-api-key.md) | GET |  |
| [List API Keys](actions/list-api-keys.md) | GET |  |

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Connection Logs](actions/list-connection-logs.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Company](actions/get-current-company.md) | GET |  |
| [Get Current Company Full Info](actions/get-current-company-full-info.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | GET |  |
| [Get Connection Properties](actions/get-connection-properties.md) | GET |  |
| [List Connections](actions/list-connections.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Connection Groups](actions/list-connection-groups.md) | GET |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Add Table Row](actions/add-table-row.md) | POST |  |
| [Delete Table Row](actions/delete-table-row.md) | DELETE |  |
| [Delete Table Rows](actions/delete-table-rows.md) | DELETE |  |
| [Get Table Row By Primary Key](actions/get-table-row-by-primary-key.md) | GET |  |
| [List Table Rows](actions/list-table-rows.md) | GET |  |
| [Search Table Rows](actions/search-table-rows.md) | GET |  |
| [Update Table Row](actions/update-table-row.md) | PUT |  |
| [Update Table Rows](actions/update-table-rows.md) | PUT |  |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Structure](actions/get-table-structure.md) | GET |  |
| [List Connection Tables](actions/list-connection-tables.md) | GET |  |
| [List Connection Tables V2](actions/list-connection-tables-v2.md) | GET |  |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Filter](actions/get-table-filter.md) | GET |  |
| [List Table Filters](actions/list-table-filters.md) | GET |  |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [List Saved Queries](actions/list-saved-queries.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User Session Settings](actions/get-user-session-settings.md) | GET |  |
| [List Company Users](actions/list-company-users.md) | GET |  |
| [List Connection Users](actions/list-connection-users.md) | GET |  |

