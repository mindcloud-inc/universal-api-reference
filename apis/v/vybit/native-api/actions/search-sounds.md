# Search Sounds with Vybit

## Endpoint

- **Method:** `GET`
- **Path:** `/sounds`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Search Sounds](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of records to return |
| `offset` | query | `number` | no | Number of records to skip for pagination |
| `search` | query | `string` | no | Search query for sound name or description |
