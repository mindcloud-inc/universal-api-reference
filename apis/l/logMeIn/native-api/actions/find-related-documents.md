# Find Related Documents with LogMeIn

Finds related knowledge base documents in LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/resolve/knowledge-base/v2/documents/:documentId/related`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Find Related Documents](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Required document ID. |
| `limit` | query | `number` | no | Maximum number of related documents to return. |
| `minScore` | query | `number` | no | Minimum relevance score between 0 and 1. |
| `tenantIds` | query | `string` | no | Comma-separated tenant IDs to filter by. |
