# List Person Updates with TVMaze Schedule

Retrieves person update timestamps from TVMaze.

## Endpoint

- **Method:** `GET`
- **Path:** `/updates/people`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Person Updates](https://www.tvmaze.com/api#person-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `string` | no | Optional update window: day, week, or month. |
