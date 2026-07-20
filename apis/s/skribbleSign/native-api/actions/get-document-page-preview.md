# Get Document Page Preview with Skribble Sign

Retrieves a document page preview from Skribble Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/documents/:documentId/pages/:pageId`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Get Document Page Preview](https://api-doc.skribble.com/#f168728b-dccb-4c6c-ad22-8120ab2cddff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The document ID. |
| `pageId` | path | `number` | yes | The document page number. |
