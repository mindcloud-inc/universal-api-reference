# Get Actions in Date Range with Week Plan

## Endpoint

- **Method:** `GET`
- **Path:** `actions/timerange`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Get Actions in Date Range](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | End date in YYYY-MM-DD format. |
| `start` | query | `string` | yes | Start date in YYYY-MM-DD format. |
| `workspaceId` | query | `number` | yes | The workspace to read actions from. |
