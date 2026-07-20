# List Collection Media with Pexels

Retrieves media from a Pexels collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/collections/:id`
- **Base URL:** `https://api.pexels.com`
- **Official documentation:** [List Collection Media](https://www.pexels.com/api/documentation/#collections-media)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Pexels collection ID. |
| `type` | query | `string` | no | Optional media filter: photos or videos. |
| `sort` | query | `string` | no | Order of media in the collection: asc or desc. Defaults to asc. |
