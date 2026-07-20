# Update Document Metadata with swiDOC

Updates document metadata in swiDOC by document ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documents/:documentId/metadata`
- **Base URL:** `https://app.swidoc.ch/api/v1`
- **Official documentation:** [Update Document Metadata](https://api.docs.swidoc.ch/swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Unique ID of the document whose metadata should be updated. |
| `fileName` | body | `string` | no | Optional new file name including extension. |
| `filePath` | body | `string` | no | Optional new folder path. |
| `description` | body | `string` | no | Optional document description. |
| `tags[]` | body | `array<string>` | no | Optional replacement tag delta for the document. Send multiple values as a array. |
| `archiveDuration` | body | `number` | no | Optional milliseconds by which the archiving duration should be extended. |
| `searchAttributes[]` | body | `array<object>` | no | Optional array of search attribute objects. |
