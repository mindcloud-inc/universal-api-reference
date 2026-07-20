# Find Related Documents By Text with LogMeIn

Finds related knowledge base documents in LogMeIn by text.

## Endpoint

- **Method:** `POST`
- **Path:** `/resolve/knowledge-base/v2/documents/related`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Find Related Documents By Text](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Required text to find semantically related documents for. |
| `limit` | query | `number` | no | Maximum number of related documents to return. |
| `minScore` | query | `number` | no | Minimum relevance score between 0 and 1. |
| `tenantIds` | query | `string` | no | Comma-separated tenant IDs to filter by. |
