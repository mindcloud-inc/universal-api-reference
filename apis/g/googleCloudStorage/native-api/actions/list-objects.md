# List Objects with Google Cloud Storage

Retrieves a list of objects from Google Cloud Storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/v1/b/:bucket/o`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [List Objects](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket to list objects from. |
| `prefix` | query | `string` | no | Return objects whose names begin with this prefix. |
| `delimiter` | query | `string` | no | Delimiter used to emulate directory-style listings. |
| `matchGlob` | query | `string` | no | Glob pattern for object names. |
