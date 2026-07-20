# Update Bucket with Google Cloud Storage

Updates an existing bucket in Google Cloud Storage.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/storage/v1/b/:bucket`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Update Bucket](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket name. |
| `labels` | body | `object` | no | Bucket labels object to patch. |
| `storageClass` | body | `list<string>` | no | Default storage class to patch. Accepted values: `ARCHIVE`, `COLDLINE`, `NEARLINE`, `RAPID`, `STANDARD`. |
