# Add Envelope Document with Sign.Plus

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/:envelope_id/document`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Add Envelope Document](https://apidoc.sign.plus/api-reference/endpoints/signplus/add-envelope-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `file` | body | `file` | yes |
