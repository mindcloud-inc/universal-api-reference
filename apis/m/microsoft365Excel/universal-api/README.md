# <img src="https://images.mindcloud.co/apps/icons/microsoft-icon_1776116407266.png" alt="Microsoft 365 Excel logo" width="28" height="28"> Microsoft 365 Excel: Universal API

Access Microsoft 365 Excel workbook files through Microsoft Graph, including OneDrive-backed workbook, worksheet, and range operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoft365Excel/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/microsoft-365/excel
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/excel?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Chart

| Action | Method | Description |
| --- | --- | --- |
| [Add Chart](actions/add-chart.md) | POST | Creates a chart in a Microsoft 365 Excel worksheet. |
| [List Charts](actions/list-charts.md) | GET | Retrieves charts from a worksheet in Microsoft 365 Excel. |

### Chart Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Chart Image](actions/get-chart-image.md) | GET | Retrieves a chart image from Microsoft 365 Excel. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Workbook Tables](actions/list-workbook-tables.md) | GET | Retrieves tables from a Microsoft 365 Excel workbook. |

### Range

| Action | Method | Description |
| --- | --- | --- |
| [Clear Range](actions/clear-range.md) | PUT | Clears a worksheet range in Microsoft 365 Excel. |
| [Get Range](actions/get-range.md) | GET | Retrieves a worksheet range from Microsoft 365 Excel. |
| [Get Used Range](actions/get-used-range.md) | GET | Retrieves the used range from a Microsoft 365 Excel worksheet. |
| [Update Range Values](actions/update-range-values.md) | PUT | Updates worksheet range values in Microsoft 365 Excel. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a table in a Microsoft 365 Excel worksheet. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from a worksheet in Microsoft 365 Excel. |

### Table Row

| Action | Method | Description |
| --- | --- | --- |
| [Add Table Rows](actions/add-table-rows.md) | POST | Adds rows to a Microsoft 365 Excel table. |
| [List Table Rows](actions/list-table-rows.md) | GET | Retrieves rows from a Microsoft 365 Excel table. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves the signed-in Microsoft 365 user profile. |

### Workbook Application

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Workbook](actions/calculate-workbook.md) | PUT | Calculates formulas in a Microsoft 365 Excel workbook. |
| [Get Workbook Application](actions/get-workbook-application.md) | GET | Retrieves workbook application details from Microsoft 365 Excel. |

### Workbook Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Workbook Session](actions/create-workbook-session.md) | POST | Creates a workbook session in Microsoft 365 Excel. |

### Workbooks

| Action | Method | Description |
| --- | --- | --- |
| [Replace Workbook Contents](actions/replace-workbook-contents.md) | PUT | Replaces workbook file contents in Microsoft 365 Excel. |
| [Upload Workbook](actions/upload-workbook.md) | POST | Uploads a workbook file to Microsoft 365 Excel. |

### Worksheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Worksheet in Workbook](actions/create-worksheet-in-workbook.md) | POST | Creates a worksheet in a Microsoft 365 Excel workbook. |
| [Delete Worksheet](actions/delete-worksheet.md) | DELETE | Deletes a worksheet from a Microsoft 365 Excel workbook. |
| [Get Worksheet](actions/get-worksheet.md) | GET | Retrieves a worksheet from a Microsoft 365 Excel workbook. |
| [List Worksheets](actions/list-worksheets.md) | GET | Retrieves worksheets from a Microsoft 365 Excel workbook. |
| [Update Worksheet](actions/update-worksheet.md) | PUT | Updates a worksheet in a Microsoft 365 Excel workbook. |

