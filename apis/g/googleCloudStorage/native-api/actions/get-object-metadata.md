# Get Object Metadata with Google Cloud Storage

Retrieves object metadata from Google Cloud Storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/v1/b/:bucket/o/:object`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Get Object Metadata](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket name. |
| `object` | path | `string` | yes | Object name. |
