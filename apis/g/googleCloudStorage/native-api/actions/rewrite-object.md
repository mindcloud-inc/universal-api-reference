# Rewrite Object with Google Cloud Storage

Rewrites an object to a destination in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/v1/b/:sourceBucket/o/:sourceObject/rewriteTo/b/:destinationBucket/o/:destinationObject`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Rewrite Object](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/rewrite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceBucket` | path | `list<string>` | yes | Bucket containing the source object. |
| `sourceObject` | path | `string` | yes | Source object name. |
| `destinationBucket` | path | `list<string>` | yes | Bucket to rewrite the object into. |
| `destinationObject` | path | `string` | yes | Destination object name. |
| `rewriteToken` | query | `string` | no | Token returned by a prior rewrite call when the rewrite is incomplete. |
