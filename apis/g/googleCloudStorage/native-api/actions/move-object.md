# Move Object with Google Cloud Storage

Moves an object within a bucket in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/v1/b/:bucket/o/:sourceObject/moveTo/o/:destinationObject`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Move Object](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/move)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket containing the object. |
| `sourceObject` | path | `string` | yes | Current object name. |
| `destinationObject` | path | `string` | yes | New object name. |
