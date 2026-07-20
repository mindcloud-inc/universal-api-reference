# Create Document with LogMeIn

Creates a new knowledge base document in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/resolve/knowledge-base/v2/documents`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Create Document](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Required document title. |
| `file` | body | `file` | no | PDF file for file documents. Mutually exclusive with content. |
| `content` | body | `string` | no | Markdown content for text documents. Mutually exclusive with file. |
| `tenantIds` | body | `string` | no | Comma-separated tenant IDs for the document. |
| `labels` | body | `string` | no | Comma-separated labels for the document. |
| `visibility` | body | `string` | no | Document visibility. |
| `folderId` | body | `string` | no | Folder ID to place the document in. |
