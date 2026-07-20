# Upload Extension with Elastic Cloud

Uploads an extension archive to Elastic Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deployments/extensions/:extension_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Upload Extension](https://www.elastic.co/docs/api/doc/cloud/operation/operation-upload-extension)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extension_id` | path | `string` | yes | Identifier for the extension. |
| `file` | body | `file` | yes | Zip file that contains the extension. |
