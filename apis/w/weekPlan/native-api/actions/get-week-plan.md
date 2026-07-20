# Get Week Plan with Week Plan

## Endpoint

- **Method:** `GET`
- **Path:** `plans`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Get Week Plan](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Day` | query | `number` | yes | Calendar day used to anchor the requested week. |
| `Month` | query | `number` | yes | Calendar month for the requested week. |
| `WorkspaceId` | query | `number` | yes | The workspace to read the week plan for. |
| `Year` | query | `number` | yes | Calendar year for the requested week. |
