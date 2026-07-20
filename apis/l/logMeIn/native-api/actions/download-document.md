# Download Document with LogMeIn

Downloads a knowledge base document from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/resolve/knowledge-base/v2/documents/:documentId/download`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Download Document](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Required document ID. |
| `inline` | query | `boolean` | no | Whether to display the file inline instead of downloading. |
| `draft` | query | `boolean` | no | Whether to download the draft version instead of the published document. |
