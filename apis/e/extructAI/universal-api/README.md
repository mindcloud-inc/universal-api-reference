# <img src="https://images.mindcloud.co/apps/icons/id-mfq-a1sad-logos_1775851254409.jpeg" alt="Extruct AI logo" width="28" height="28"> Extruct AI: Universal API

Company discovery and research platform for finding, enriching, and evaluating companies.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/extructAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.extruct.ai
- **Vendor API docs:** https://docs.extruct.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Find Similar Companies](actions/find-similar-companies.md) | GET | Finds similar companies in Extruct AI. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Extruct AI. |

### Discovery Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Discovery Task](actions/create-discovery-task.md) | POST | Creates a discovery task in Extruct AI. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Healthcheck](actions/healthcheck.md) | GET | Retrieves API health status from Extruct AI. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Clone Table](actions/clone-table.md) | POST | Clones a table in Extruct AI. |
| [Create Table](actions/create-table.md) | POST | Creates a table in Extruct AI. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes a table from Extruct AI. |
| [Get Table](actions/get-table.md) | GET | Retrieves a table from Extruct AI. |
| [Get Table Data](actions/get-table-data.md) | GET | Retrieves table data from Extruct AI. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from Extruct AI. |
| [Update Table](actions/update-table.md) | PUT | Updates a table in Extruct AI. |

### Table Column

| Action | Method | Description |
| --- | --- | --- |
| [Create Table Columns](actions/create-table-columns.md) | POST | Creates table columns in Extruct AI. |
| [Delete Table Column](actions/delete-table-column.md) | DELETE | Deletes a table column from Extruct AI. |
| [Update Table Column](actions/update-table-column.md) | PUT | Updates a table column in Extruct AI. |

### Table Row

| Action | Method | Description |
| --- | --- | --- |
| [Add Input Data](actions/add-input-data.md) | POST | Adds input data rows to a table in Extruct AI. |
| [Delete Table Rows](actions/delete-table-rows.md) | DELETE | Deletes table rows from Extruct AI. |
| [Get Row Data](actions/get-row-data.md) | GET | Retrieves table row data from Extruct AI. |
| [Update Table Rows](actions/update-table-rows.md) | PUT | Updates table rows in Extruct AI. |

### Table Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Enrichment](actions/run-enrichment.md) | POST | Runs enrichment on a table in Extruct AI. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Discovery Task](actions/get-discovery-task.md) | GET | Retrieves a discovery task from Extruct AI. |
| [Get Discovery Task Results](actions/get-discovery-task-results.md) | GET | Retrieves discovery task results from Extruct AI. |
| [List Discovery Tasks](actions/list-discovery-tasks.md) | GET | Retrieves discovery tasks from Extruct AI. |
| [Resume Discovery Task](actions/resume-discovery-task.md) | PUT | Resumes a discovery task in Extruct AI. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the authenticated user from Extruct AI. |

