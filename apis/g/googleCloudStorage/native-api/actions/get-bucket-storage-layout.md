# Get Bucket Storage Layout with Google Cloud Storage

Retrieves a bucket's storage layout from Google Cloud Storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/v1/b/:bucket/storageLayout`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Get Bucket Storage Layout](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/getStorageLayout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket name. |
| `prefix` | query | `string` | no | Object-name prefix for storage layout evaluation. |
