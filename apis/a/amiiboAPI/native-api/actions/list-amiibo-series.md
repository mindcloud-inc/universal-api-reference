# List Amiibo Series with Amiibo API

## Endpoint

- **Method:** `GET`
- **Path:** `/api/amiiboseries/`
- **Base URL:** `https://amiiboapi.com`
- **Official documentation:** [List Amiibo Series](https://github.com/N3evin/AmiiboAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Optional series name filter. |
| `sort` | query | `string` | no | Comma-separated source-defined fields: key or name. |
