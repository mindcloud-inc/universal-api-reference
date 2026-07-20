# Search Tracks with Audius

Finds tracks in Audius by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/tracks/search`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Search Tracks](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The search query. |
| `limit` | query | `number` | no | The number of items to fetch. |
