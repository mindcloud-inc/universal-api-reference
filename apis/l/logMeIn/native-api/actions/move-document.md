# Move Document with LogMeIn

Moves an existing knowledge base document in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/resolve/knowledge-base/v2/documents/:documentId/move`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Move Document](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Required document ID. |
| `folderId` | body | `string` | yes | Target folder ID. Send null to move the document to root. |
