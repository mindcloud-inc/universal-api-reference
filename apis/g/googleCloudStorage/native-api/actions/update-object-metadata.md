# Update Object Metadata with Google Cloud Storage

Updates object metadata in Google Cloud Storage.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/storage/v1/b/:bucket/o/:object`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Update Object Metadata](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket name. |
| `object` | path | `string` | yes | Object name. |
| `metadata` | body | `object` | no | Custom object metadata object. |
| `contentType` | body | `string` | no | Object content type metadata. |
| `cacheControl` | body | `string` | no | Cache-Control directive for the object data. |
| `contentDisposition` | body | `string` | no | Content-Disposition value for the object data. |
| `contentEncoding` | body | `string` | no | Content-Encoding value for the object data. |
| `contentLanguage` | body | `string` | no | Content-Language value for the object data. |
| `customTime` | body | `date` | no | User-specified object timestamp in RFC 3339 format. |
| `eventBasedHold` | body | `boolean` | no | Whether the object is subject to an event-based hold. |
| `temporaryHold` | body | `boolean` | no | Whether the object is subject to a temporary hold. |
| `retention` | body | `object` | no | Object retention configuration. |
| `mode` | body | `list<string>` | no | Object retention mode. Accepted values: `Locked`, `Unlocked`. |
| `retainUntilTime` | body | `date` | no | Earliest time the object can be deleted or replaced, in RFC 3339 format. |
