# Get Document Metadata with swiDOC

Retrieves document metadata from swiDOC by document ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId/metadata`
- **Base URL:** `https://app.swidoc.ch/api/v1`
- **Official documentation:** [Get Document Metadata](https://api.docs.swidoc.ch/swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Unique ID of the document whose metadata should be retrieved. |
