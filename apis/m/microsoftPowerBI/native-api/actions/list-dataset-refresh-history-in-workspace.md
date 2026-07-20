# List Dataset Refresh History in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/refreshes`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Dataset Refresh History in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-history-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `datasetId` | path | `string` | yes | The Power BI dataset ID. |
| `$top` | query | `number` | no | The requested number of entries in the refresh history. If omitted, Power BI returns the last available 60 entries. |
