# List Events History with Restream

Retrieves past events from Restream.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/events/history`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [List Events History](https://developers.restream.io/events/events-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of history items to return. |
| `page` | query | `number` | no | History page number. |
