# List Events with Communi App

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/event`
- **Base URL:** `https://api.communiapp.de`
- **Official documentation:** [List Events](https://api.communiapp.de/docs#/Event/get_rest_event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | query | `number` | yes | The CommuniApp group ID. The endpoint requires a group context for event listings. |
| `search` | query | `string` | no | Optional full-text search across event title, description, and location. |
