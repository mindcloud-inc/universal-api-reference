# Create Purge with imgix

Purges an asset from the imgix cache.

## Endpoint

- **Method:** `POST`
- **Path:** `purge`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Create Purge](https://docs.imgix.com/en-US/apis/management/purges)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.source_id` | body | `string` | no | Required when purging a sub-image. |
| `data.attributes.sub_image` | body | `boolean` | no | Set true to purge a sub-image and parent derivatives. |
| `data.attributes.url` | body | `string` | yes | The fully qualified imgix asset URL to purge. |
