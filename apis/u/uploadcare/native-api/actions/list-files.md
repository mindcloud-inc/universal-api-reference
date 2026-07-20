# List Files with Uploadcare

Retrieves all files from your Uploadcare project.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [List Files](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/filesList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Start listing files uploaded after this ISO 8601 timestamp. |
| `include` | query | `string` | no | Include extra fields such as appdata in the file object. |
| `ordering` | query | `string` | no | Sort order for returned files. |
| `removed` | query | `boolean` | no | Set true to only include removed files. |
| `stored` | query | `boolean` | no | Set true to only include stored files, or false for temporary files. |
