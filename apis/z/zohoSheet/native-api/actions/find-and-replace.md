# Find and Replace with Zoho Sheet

Finds and replaces matching content in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Find and Replace](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Find-and-replace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `search` | body | `string` | yes | The string that needs to be replaced |
| `replace_with` | body | `string` | yes | New replaced string |
| `scope` | body | `string` | yes | workbook \| worksheet \| row \| column |
| `worksheet_name` | body | `string` | no | Required if the scope is either worksheet, or row, or column |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `row` | body | `number` | no | Required if the scope is row |
| `column` | body | `number` | no | Required if the scope is column |
| `is_case_sensitive` | body | `boolean` | no | If set to true upper case and lower case characters will be different during search. By default it is false |
| `is_exact_match` | body | `boolean` | no | If set to true the search with will match with the full content of the cell. |
