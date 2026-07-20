# Word Extract Text with Encodian

Extracts text from a Word document in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Word/GetTextFromWord`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Word Extract Text](https://support.encodian.com/hc/en-gb/articles/10583756977180)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | The file content of the source Microsoft Word file. |
| `startPage` | body | `number` | no | Sets the page number to begin text extraction from. |
| `endPage` | body | `number` | no | Sets the page number to end text extraction from. |
| `removeComments` | body | `boolean` | no | Set whether comments should be removed prior to extracting text. |
| `acceptChanges` | body | `boolean` | no | Set whether tracked changes should be accepted prior to extracting text. |
