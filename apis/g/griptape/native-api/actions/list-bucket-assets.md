# List Bucket Assets with Griptape

Finds assets in a Griptape bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/buckets/:bucket_id/assets`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [List Bucket Assets](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket_id` | path | `string` | yes | The bucket ID whose assets should be listed. |
| `postfix` | query | `string` | no | Optional asset key postfix to filter results. |
| `prefix` | query | `string` | no | Optional asset key prefix to filter results. |
