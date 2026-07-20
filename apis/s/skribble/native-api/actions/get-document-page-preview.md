# Get Document Page Preview with Skribble

Retrieves a preview image for a document page in Skribble.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/documents/:documentId/pages/:pageId`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Get Document Page Preview](https://api-doc.skribble.com/#f168728b-dccb-4c6c-ad22-8120ab2cddff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Skribble document ID. |
| `pageId` | path | `string` | yes | The page index starting at 0. |
| `scale` | query | `number` | no | Preview scale percentage, such as 20 or 100. |
