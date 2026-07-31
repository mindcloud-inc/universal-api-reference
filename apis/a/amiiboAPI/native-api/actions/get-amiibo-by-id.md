# Get Amiibo by ID with Amiibo API

## Endpoint

- **Method:** `GET`
- **Path:** `/api/amiibo/`
- **Base URL:** `https://amiiboapi.com`
- **Official documentation:** [Get Amiibo by ID](https://github.com/N3evin/AmiiboAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Required 16-digit hexadecimal Amiibo ID, optionally 0x-prefixed. |
