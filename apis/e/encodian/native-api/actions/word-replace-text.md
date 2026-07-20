# Word Replace Text with Encodian

Replaces text in a Word document with Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Word/WordSearchAndReplaceText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Word Replace Text](https://support.encodian.com/hc/en-gb/articles/15949925002268)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The filename of the source Word document including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the source Word document. |
| `Phrases[]` | body | `array<object>` | yes | An array of phrases containing the search and replacement instructions. |
| `ReturnFile` | body | `boolean` | no | Set whether to return the file or just an operation ID. |
