# Get Document with Basecamp

Retrieves a document from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/documents/:documentId.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Document](https://github.com/basecamp/bc3-api/blob/master/sections/documents.md#get-a-document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `documentId` | path | `number` | yes |
