# Get Meme Items with KLIPY

Retrieves memes from KLIPY by ID or slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/static-memes/items`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [Get Meme Items](https://docs.klipy.com/memes-api/memes-items-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids` | query | `string` | no |
| `slugs` | query | `string` | no |
