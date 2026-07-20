# Restore Object with Google Cloud Storage

Restores a soft-deleted object in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/v1/b/:bucket/o/:object/restore`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Restore Object](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/restore)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket containing the soft-deleted object. |
| `object` | path | `string` | yes | Soft-deleted object name. |
| `generation` | query | `string` | yes | Generation of the soft-deleted object to restore. |
