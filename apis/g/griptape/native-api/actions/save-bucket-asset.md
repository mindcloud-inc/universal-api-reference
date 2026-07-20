# Save Bucket Asset with Griptape

Creates a bucket asset record in Griptape.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/buckets/:bucket_id/assets`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Save Bucket Asset](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket_id` | path | `string` | yes | The bucket ID to save the asset in. |
| `name` | body | `string` | yes | The full asset key to create in the bucket. |
