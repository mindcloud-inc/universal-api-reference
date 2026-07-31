# Search Amiibo with Amiibo API

## Endpoint

- **Method:** `GET`
- **Path:** `/api/amiibo/`
- **Base URL:** `https://amiiboapi.com`
- **Official documentation:** [Search Amiibo](https://github.com/N3evin/AmiiboAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `head` | query | `string` | no | 8-digit hexadecimal head identifier. |
| `tail` | query | `string` | no | 8-digit hexadecimal tail identifier. |
| `name` | query | `string` | no | Amiibo name filter. |
| `gameseries` | query | `string` | no | Game series name or 0x-prefixed hexadecimal game-series key. |
| `switch_titleid` | query | `string` | no | Nintendo Switch title ID filter. |
| `wiiu_titleid` | query | `string` | no | Wii U title ID filter. |
| `3ds_titleid` | query | `string` | no | Nintendo 3DS title ID filter. |
| `character` | query | `string` | no | Character name or 0x-prefixed hexadecimal character key. |
| `variant` | query | `string` | no | 6-digit hexadecimal variant key. |
| `type` | query | `string` | no | Amiibo type name or 0x-prefixed hexadecimal type key. |
| `amiibo_model` | query | `string` | no | 4-digit hexadecimal amiibo-model key. |
| `amiiboSeries` | query | `string` | no | Amiibo series name or 0x-prefixed hexadecimal series key. |
| `sort` | query | `string` | no | Comma-separated source-defined sort fields, such as name, gameseries, character, type, series, or release_na. |
