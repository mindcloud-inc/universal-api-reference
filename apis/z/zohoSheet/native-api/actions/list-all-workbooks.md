# List All Workbooks with Zoho Sheet

Retrieves all workbooks from Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/workbooks`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [List All Workbooks](https://www.zoho.com/sheet/help/api/v2/#WORKBOOK-List-all-workbooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_index` | body | `number` | no | Optional Parameter. This parameter can be used to get a few resources if there are too many. |
| `count` | body | `number` | no | Optional Parameter. It denotes the number of resources in response. |
| `sort_option` | body | `string` | no | Optional Parameter. Supported options are 'recently_opened', 'recently_modified', 'recently_created', 'ascending', and 'descending'. Default option is 'recently_created'. |
