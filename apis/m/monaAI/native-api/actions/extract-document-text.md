# Extract Document Text with Mona AI

Extracts text from a document in Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/parsing/AnyDocumentToText`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Extract Document Text](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentData` | body | `string` | no | Inline document data to extract when no URL is used. |
| `documentUrl` | body | `string` | no | URL of the document to extract text from. |
| `options` | body | `object` | no | Document extraction options object. |
| `permission` | body | `string` | yes | Mona permission string required by the document extraction endpoint. |
