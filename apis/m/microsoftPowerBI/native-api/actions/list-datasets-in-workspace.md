# List Datasets in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/datasets`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Datasets in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-datasets-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
