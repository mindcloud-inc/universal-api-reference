# Get Scout Updates with Yutori

Retrieves updates for a specific scout in Yutori.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scouting/tasks/:scout_id/updates`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Get Scout Updates](https://docs.yutori.com/reference/scouts-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
| `page_size` | query | `number` | no | Maximum number of updates to return. |
| `cursor` | query | `string` | no | Cursor for the next page of updates. |
