# Copy Object with Google Cloud Storage

Copies an object to a destination in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/v1/b/:sourceBucket/o/:sourceObject/copyTo/b/:destinationBucket/o/:destinationObject`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Copy Object](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceBucket` | path | `list<string>` | yes | Bucket containing the source object. |
| `sourceObject` | path | `string` | yes | Source object name. |
| `destinationBucket` | path | `list<string>` | yes | Bucket to copy the object into. |
| `destinationObject` | path | `string` | yes | Destination object name. |
| `metadata` | body | `object` | no | Optional replacement custom metadata. |
