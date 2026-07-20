# Update Draft Document with LogMeIn

Updates an existing draft document in LogMeIn.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/resolve/knowledge-base/v2/drafts/:draftId`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Update Draft Document](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draftId` | path | `string` | yes | Required draft ID. |
| `file` | body | `file` | no | PDF file replacement for file drafts. Mutually exclusive with content. |
| `title` | body | `string` | no | New title for the draft. |
| `content` | body | `string` | no | New Markdown content for text drafts. Mutually exclusive with file. |
| `tenantIds` | body | `string` | no | Comma-separated tenant IDs for the draft. |
| `labels` | body | `string` | no | Comma-separated labels for the draft. |
