# List Amiibo Type with Amiibo API

## Endpoint

- **Method:** `GET`
- **Path:** `/api/type/`
- **Base URL:** `https://amiiboapi.com`
- **Official documentation:** [List Amiibo Type](https://github.com/N3evin/AmiiboAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Optional Amiibo type name filter. |
| `sort` | query | `string` | no | Comma-separated source-defined fields: key or name. |
