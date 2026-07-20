# Get Bucket Asset URL with Griptape

Retrieves a signed bucket asset URL from Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/buckets/:bucket_id/asset-urls/:full_key`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Get Bucket Asset URL](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket_id` | path | `string` | yes | The bucket ID containing the asset. |
| `full_key` | path | `string` | yes | The full asset key to generate a URL for. |
