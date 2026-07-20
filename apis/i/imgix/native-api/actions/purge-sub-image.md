# Purge Sub-image with imgix

Purges a sub-image from the imgix cache.

## Endpoint

- **Method:** `POST`
- **Path:** `purge`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Purge Sub-image](https://docs.imgix.com/en-US/apis/management/purges)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.source_id` | body | `string` | yes | The imgix source_id for the sub-image asset. |
| `data.attributes.url` | body | `string` | yes | The fully qualified imgix asset URL to purge. |
