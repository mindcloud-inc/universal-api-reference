# Refresh Dataset in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/refreshes`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Refresh Dataset in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/refresh-dataset-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `datasetId` | path | `string` | yes | The Power BI dataset ID. |
| `notifyOption` | body | `list` | no | Mail notification option for the refresh request. Accepted values: `0`, `1`, `2`. |
