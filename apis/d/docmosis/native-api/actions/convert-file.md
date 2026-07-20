# Convert File with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/convert`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Convert File](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=53)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file to convert. |
| `outputName` | body | `string` | yes | Output filename including desired extension, for example output.pdf. |
