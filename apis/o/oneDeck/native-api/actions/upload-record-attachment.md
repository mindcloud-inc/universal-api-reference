# Upload Record Attachment with OneDeck

Uploads an attachment to a OneDeck board record.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards/{{boardId}}/records/{{recordId}}/attachments`
- **Base URL:** `https://{accountName}.onedeck.com/api/v1`
- **Official documentation:** [Upload Record Attachment](https://www.onedeck.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | path | `string` | yes | The OneDeck board ID. |
| `recordId` | path | `string` | yes | The OneDeck record ID. |
| `fileName` | body | `string` | yes | The file name to send in the x-file-name header. |
| `contentType` | body | `string` | yes | The MIME type for the attachment. |
| `fileContent` | body | `string` | yes | Raw text content to upload as the attachment body. |
