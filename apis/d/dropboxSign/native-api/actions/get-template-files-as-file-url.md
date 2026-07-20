# Get Template Files as File URL with Dropbox Sign

Retrieves template files as file URLs from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/files_as_file_url/:template_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Template Files as File URL](https://developers.hellosign.com/api/reference/operation/templateFilesAsFileUrl/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `force_download` | query | `number` | no | Set to 0 to display the PDF in the browser instead of downloading it. |
| `template_id` | path | `string` | yes | The ID of the template to retrieve files for. |
