# Upload Product File with Rithum for Brands

Should send a XML template to bulk update items

## Endpoint

- **Method:** `POST`
- **Path:** `ProductUpload`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Upload Product File](https://api.channeladvisor.com/apidocs#tag/ProductUpload/operation/ProductUpload_UploadFile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uploadFile` | body | `file` | yes |
| `profileId` | query | `list<number>` | no |
| `templateCode` | query | `string` | no |
| `importType` | query | `number` | no |
