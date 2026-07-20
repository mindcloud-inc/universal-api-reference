# Mark Document as Read with Recommand

Updates a Recommand document as read.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/documents/:documentId/mark-as-read`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Mark Document as Read](https://recommand.eu/en/reference/documents/mark-document-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | documentId parameter. |
| `read` | body | `boolean` | no | Whether to mark the document as read (true) or unread (false). If not provided, defaults to true. |
