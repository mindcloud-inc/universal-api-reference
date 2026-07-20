# File Replace Text With Image with Encodian - General

Replaces text placeholders with images in a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/SearchAndReplaceTextWithImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [File Replace Text With Image](https://support.encodian.com/hc/en-gb/articles/360027234874)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | no | Source filename including extension. |
| `FileContent` | body | `string` | no | Base64-encoded source file content. |
| `imageFilename` | body | `string` | yes | Filename for the replacement image. |
| `SearchText` | body | `string` | yes | Text token or value to replace. |
| `imageFileContent` | body | `string` | yes | Base64-encoded replacement image content. |
