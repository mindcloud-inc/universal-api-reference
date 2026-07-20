# Get Day Actions with Week Plan

## Endpoint

- **Method:** `GET`
- **Path:** `actions/day`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Get Day Actions](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Day` | query | `number` | yes | Calendar day of month for the requested day. |
| `Month` | query | `number` | yes | Calendar month for the requested day. |
| `workspaceId` | query | `number` | yes | The workspace to read actions from. |
| `Year` | query | `number` | yes | Calendar year for the requested day. |
