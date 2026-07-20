# <img src="https://images.mindcloud.co/apps/icons/id-uk69wm-ys-logos_1773174570537.png" alt="Smartsheet logo" width="28" height="28"> Smartsheet: Universal API

Manage Smartsheet sheets, rows, workspaces, and dashboards

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartSheet/latest
- **Category:** Productivity / Project Management
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smartsheet.com
- **Vendor API docs:** https://developers.smartsheet.com/api/smartsheet/openapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Row](actions/get-row.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-row?connectionId=$CONNECTION_ID&sheetId=1&rowId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Link Attachment on Sheet](actions/create-link-attachment-on-sheet.md) | POST | Creates a link attachment on a Smartsheet sheet. |
| [List Sheet Attachments](actions/list-sheet-attachments.md) | GET | Retrieves attachments from a Smartsheet sheet. |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [Create Column](actions/create-column.md) | POST | Creates a new column in a Smartsheet sheet. |
| [Delete Column](actions/delete-column.md) | DELETE | Deletes an existing column from a Smartsheet sheet. |
| [List Columns](actions/list-columns.md) | GET | Retrieves columns from a Smartsheet sheet. |
| [Update Column](actions/update-column.md) | PUT | Updates an existing column in a Smartsheet sheet. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder in Workspace](actions/create-folder-in-workspace.md) | POST | Creates a new folder in a Smartsheet workspace. |

### Folder Child

| Action | Method | Description |
| --- | --- | --- |
| [List Folder Children](actions/list-folder-children.md) | GET | Retrieves items in a Smartsheet folder. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from Smartsheet. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Copy Rows](actions/copy-rows.md) | POST | Copies rows to another sheet in Smartsheet. |
| [Create Row](actions/create-row.md) | POST | Creates a new row in a Smartsheet sheet. |
| [Delete Rows](actions/delete-rows.md) | DELETE | Deletes rows from a Smartsheet sheet. |
| [Get Row](actions/get-row.md) | GET | Retrieves a row from a Smartsheet sheet. |
| [Move Rows](actions/move-rows.md) | PUT | Moves rows to another sheet in Smartsheet. |
| [Sort Sheet Rows](actions/sort-sheet-rows.md) | PUT | Sorts rows in a Smartsheet sheet. |
| [Update Row](actions/update-row.md) | PUT | Updates a row in a Smartsheet sheet. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Smartsheet](actions/search-smartsheet.md) | GET | Finds matching items in Smartsheet by query. |

### Sheet

| Action | Method | Description |
| --- | --- | --- |
| [Copy Sheet](actions/copy-sheet.md) | POST | Creates a copy of a sheet in Smartsheet. |
| [Create Sheet](actions/create-sheet.md) | POST | Creates a new sheet in Smartsheet. |
| [Create Sheet in Folder](actions/create-sheet-in-folder.md) | POST | Creates a new sheet in a Smartsheet folder. |
| [Create Sheet in Workspace](actions/create-sheet-in-workspace.md) | POST | Creates a new sheet in a Smartsheet workspace. |
| [Delete Sheet](actions/delete-sheet.md) | DELETE | Deletes an existing sheet from Smartsheet. |
| [Get Sheet](actions/get-sheet.md) | GET | Retrieves a sheet from Smartsheet. |
| [List Sheets](actions/list-sheets.md) | GET | Retrieves sheets from Smartsheet. |
| [Move Sheet](actions/move-sheet.md) | PUT | Moves a sheet in Smartsheet. |
| [Update Sheet](actions/update-sheet.md) | PUT | Updates an existing sheet in Smartsheet. |

### Sheet Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Sheet Summary](actions/get-sheet-summary.md) | GET | Retrieves a sheet summary from Smartsheet. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Smartsheet. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Smartsheet. |

