# Update Document with LogMeIn

Updates an existing knowledge base document in LogMeIn.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/resolve/knowledge-base/v2/documents/:documentId`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Update Document](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Required document ID. |
| `file` | body | `file` | no | PDF file replacement for file documents. Mutually exclusive with content. |
| `title` | body | `string` | no | New title for the document. |
| `content` | body | `string` | no | New Markdown content for text documents. Mutually exclusive with file. |
| `tenantIds` | body | `string` | no | Comma-separated tenant IDs for the document. |
| `labels` | body | `string` | no | Comma-separated labels for the document. |
| `visibility` | body | `string` | no | Document visibility. |
