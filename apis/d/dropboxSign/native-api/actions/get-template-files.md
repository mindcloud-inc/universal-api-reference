# Get Template Files with Dropbox Sign

Retrieves template files from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/files/:template_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Template Files](https://developers.hellosign.com/api/reference/operation/templateFiles/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_type` | query | `string` | no | Set to pdf for a single merged document or zip for a collection of individual documents. |
| `template_id` | path | `string` | yes | The ID of the template to retrieve files for. |
