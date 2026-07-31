# Get Detailed Amiibo by Head and Tail with Amiibo API

## Endpoint

- **Method:** `GET`
- **Path:** `/api/amiibofull/`
- **Base URL:** `https://amiiboapi.com`
- **Official documentation:** [Get Detailed Amiibo by Head and Tail](https://github.com/N3evin/AmiiboAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `head` | query | `string` | yes | Required 8-digit hexadecimal head identifier. |
| `tail` | query | `string` | yes | Required 8-digit hexadecimal tail identifier. |
