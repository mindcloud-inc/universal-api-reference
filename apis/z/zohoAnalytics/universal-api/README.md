# <img src="https://images.mindcloud.co/apps/icons/zoho-analytics_1773674249190.png" alt="Zoho Analytics logo" width="28" height="28"> Zoho Analytics: Universal API

Manage Zoho Analytics workspaces, views, tables, and data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoAnalytics/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/analytics
- **Vendor API docs:** https://www.zoho.com/analytics/api/v2/introduction.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from a Zoho Analytics workspace. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves available organizations from Zoho Analytics. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create Report](actions/create-report.md) | POST | Creates a report in Zoho Analytics. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Row](actions/add-row.md) | POST | Creates a row in a Zoho Analytics table. |
| [Create Export Job From SQL](actions/create-export-job-from-sql.md) | GET | Creates a SQL export job in Zoho Analytics. |
| [Create Import Job For Existing Table](actions/create-import-job-for-existing-table.md) | POST | Creates an import job for a Zoho Analytics table. |
| [Create Query Table](actions/create-query-table.md) | POST | Creates a query table in Zoho Analytics. |
| [Create Table](actions/create-table.md) | POST | Creates a table in Zoho Analytics. |
| [Delete Rows](actions/delete-rows.md) | DELETE | Deletes rows from a Zoho Analytics table. |
| [Download Exported Data](actions/download-exported-data.md) | GET | Downloads exported data from Zoho Analytics. |
| [Export View Data](actions/export-view-data.md) | GET | Exports view data from Zoho Analytics. |
| [Get Export Job Details](actions/get-export-job-details.md) | GET | Retrieves export job details from Zoho Analytics. |
| [Get Import Job Details](actions/get-import-job-details.md) | GET | Retrieves import job details from Zoho Analytics. |
| [Get Meta Details](actions/get-meta-details.md) | GET | Retrieves workspace or view details from Zoho Analytics. |
| [Import Data Into Existing Table](actions/import-data-into-existing-table.md) | POST | Imports data into an existing Zoho Analytics table. |
| [Update Rows](actions/update-rows.md) | PUT | Updates rows in a Zoho Analytics table. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [Get View](actions/get-view.md) | GET | Retrieves a view from Zoho Analytics by ID. |
| [List Recent Views](actions/list-recent-views.md) | GET | Retrieves recently accessed views from Zoho Analytics. |
| [List Views](actions/list-views.md) | GET | Retrieves views from a Zoho Analytics workspace. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Delete View](actions/delete-view.md) | DELETE | Deletes a view from Zoho Analytics. |
| [Rename View](actions/rename-view.md) | PUT | Renames a view in Zoho Analytics. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Zoho Analytics by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves accessible workspaces from Zoho Analytics. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a workspace in Zoho Analytics. |

