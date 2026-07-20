# <img src="https://images.mindcloud.co/apps/icons/zoho-sheet_1773348581567.png" alt="Zoho Sheet logo" width="28" height="28"> Zoho Sheet: Universal API

Create and manage Zoho Sheet workbooks, worksheets, tables, and spreadsheet content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoSheet/latest
- **Category:** Content & Files / Storage
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sheet.zoho.com/
- **Vendor API docs:** https://www.zoho.com/sheet/help/api/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Workbooks](actions/list-all-workbooks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-workbooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Add Records to Table](actions/add-records-to-table.md) | POST | Adds records to a table in Zoho Sheet. |
| [Add Records to Worksheet](actions/add-records-to-worksheet.md) | POST | Adds records to a worksheet in Zoho Sheet. |
| [Create Table](actions/create-table.md) | POST | Creates a new table in Zoho Sheet. |
| [Delete Records from Table](actions/delete-records-from-table.md) | DELETE | Deletes records from a table in Zoho Sheet. |
| [Delete Records from Worksheet](actions/delete-records-from-worksheet.md) | DELETE | Deletes records from a worksheet in Zoho Sheet. |
| [Fetch Records from Table](actions/fetch-records-from-table.md) | GET | Retrieves records from a table in Zoho Sheet. |
| [Fetch Records from Worksheet](actions/fetch-records-from-worksheet.md) | GET | Retrieves records from a worksheet in Zoho Sheet. |
| [List All Tables](actions/list-all-tables.md) | GET | Retrieves tables from a Zoho Sheet workbook. |
| [Update Records in Table](actions/update-records-in-table.md) | PUT | Updates records in a table in Zoho Sheet. |
| [Update Records in Worksheet](actions/update-records-in-worksheet.md) | PUT | Updates records in a worksheet in Zoho Sheet. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Copy Workbook](actions/copy-workbook.md) | POST | Creates a copy of a workbook in Zoho Sheet. |
| [Create Workbook](actions/create-workbook.md) | POST | Creates a new workbook in Zoho Sheet. |
| [Find](actions/find.md) | GET | Finds matching content in Zoho Sheet. |
| [Find and Replace](actions/find-and-replace.md) | PUT | Finds and replaces matching content in Zoho Sheet. |
| [Get Content of Range](actions/get-content-of-range.md) | GET | Retrieves the content of a range in Zoho Sheet. |
| [Get Used Area](actions/get-used-area.md) | GET | Retrieves the used area of a worksheet in Zoho Sheet. |
| [List All Workbooks](actions/list-all-workbooks.md) | GET | Retrieves all workbooks from Zoho Sheet. |
| [Set Content to Range](actions/set-content-to-range.md) | PUT | Updates the content of a range in Zoho Sheet. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Worksheet](actions/create-worksheet.md) | POST | Creates a new worksheet in Zoho Sheet. |
| [Delete Worksheet](actions/delete-worksheet.md) | DELETE | Deletes an existing worksheet from Zoho Sheet. |
| [List All Worksheets](actions/list-all-worksheets.md) | GET | Retrieves worksheets from a Zoho Sheet workbook. |
| [Rename Worksheet](actions/rename-worksheet.md) | PUT | Renames an existing worksheet in Zoho Sheet. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List All Templates](actions/list-all-templates.md) | GET | Retrieves all templates from Zoho Sheet. |

