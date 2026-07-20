# Take Over In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/Default.TakeOver`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Take Over In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/take-over-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
