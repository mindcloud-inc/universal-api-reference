# Utilities - Clean Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/CleanString`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Clean Text](https://support.encodian.com/hc/en-gb/articles/10072015106077)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text value to process |
| `removeCharacterSet` | body | `string` | no | Set the collection of characters to remove from the text value provided |
| `removeControlChars` | body | `boolean` | no | Set whether to remove control characters from the text value |
| `removeInvalidFileNameChars` | body | `boolean` | no | Set whether to remove characters that are invalid in file names from the text value |
| `trimResult` | body | `boolean` | no | Set whether white-space should be trimmed from the processed text value |
