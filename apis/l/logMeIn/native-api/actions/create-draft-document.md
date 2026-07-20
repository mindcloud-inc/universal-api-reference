# Create Draft Document with LogMeIn

Creates a new draft document in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/resolve/knowledge-base/v2/drafts`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Create Draft Document](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | no | Existing document ID to create a draft for. Omit to create a standalone draft. |
| `file` | body | `file` | no | PDF file for file drafts. Mutually exclusive with content. |
| `title` | body | `string` | no | Draft title. Required when documentId is omitted. |
| `content` | body | `string` | no | Markdown content for text drafts. Mutually exclusive with file. |
| `tenantIds` | body | `string` | no | Comma-separated tenant IDs for the draft. |
| `labels` | body | `string` | no | Comma-separated labels for the draft. |
| `visibility` | body | `string` | no | Draft visibility. |
