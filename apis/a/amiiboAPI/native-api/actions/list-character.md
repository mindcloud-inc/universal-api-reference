# List Character with Amiibo API

## Endpoint

- **Method:** `GET`
- **Path:** `/api/character/`
- **Base URL:** `https://amiiboapi.com`
- **Official documentation:** [List Character](https://github.com/N3evin/AmiiboAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Optional character name filter. |
| `sort` | query | `string` | no | Comma-separated source-defined fields: key or name. |
