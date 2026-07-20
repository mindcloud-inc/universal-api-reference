# Get Upload File URL with Moorcheh

Generates a pre-signed file upload URL in Moorcheh.

## Endpoint

- **Method:** `POST`
- **Path:** `/namespaces/:namespace_name/upload-url`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Get Upload File URL](https://docs.moorcheh.ai/api-reference/data/upload-file-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Name of the text namespace to upload the file into. |
| `file_name` | body | `string` | yes | Target filename including extension, such as document.pdf. Moorcheh auto-detects the content type. |
