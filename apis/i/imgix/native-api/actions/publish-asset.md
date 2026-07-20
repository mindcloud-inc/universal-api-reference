# Publish Asset with imgix

Publishes an asset in imgix.

## Endpoint

- **Method:** `POST`
- **Path:** `publish`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Publish Asset](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.source_id` | body | `string` | yes | The imgix source_id for the asset. |
| `data.attributes.url` | body | `string` | yes | The full imgix URL of the asset to publish. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
