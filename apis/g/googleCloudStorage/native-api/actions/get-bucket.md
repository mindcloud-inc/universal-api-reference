# Get Bucket with Google Cloud Storage

Retrieves bucket metadata from Google Cloud Storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/v1/b/:bucket`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Get Bucket](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket name. |
