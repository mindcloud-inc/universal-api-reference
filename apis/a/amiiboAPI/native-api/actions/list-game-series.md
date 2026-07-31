# List Game Series with Amiibo API

## Endpoint

- **Method:** `GET`
- **Path:** `/api/gameseries/`
- **Base URL:** `https://amiiboapi.com`
- **Official documentation:** [List Game Series](https://github.com/N3evin/AmiiboAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Optional game-series name filter. |
| `sort` | query | `string` | no | Comma-separated source-defined fields: key or name. |
