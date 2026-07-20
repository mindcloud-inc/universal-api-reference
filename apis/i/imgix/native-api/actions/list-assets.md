# List Assets with imgix

Retrieves assets from an imgix source.

## Endpoint

- **Method:** `GET`
- **Path:** `sources/:sourceId/assets`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [List Assets](https://docs.imgix.com/en-US/apis/management/assets)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page[cursor]` | query | `string` | no | Cursor value for the next asset page. |
| `page[limit]` | query | `number` | no | Number of assets to return per page. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
