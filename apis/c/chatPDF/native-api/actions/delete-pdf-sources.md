# Delete PDF Sources with ChatPDF

## Endpoint

- **Method:** `POST`
- **Path:** `/sources/delete`
- **Base URL:** `https://api.chatpdf.com/v1`
- **Official documentation:** [Delete PDF Sources](https://www.chatpdf.com/docs/api/backend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sources[]` | body | `array<string>` | yes | Array of ChatPDF source IDs to delete. |
