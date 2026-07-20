# Archive Document with swiDOC

Archives a document in swiDOC.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.swidoc.ch/api/v1`
- **Official documentation:** [Archive Document](https://api.docs.swidoc.ch/swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 encoded file content. |
| `metadata.fileName` | body | `string` | yes | Name of the file including extension. |
| `metadata.filePath` | body | `string` | no | Optional archive folder path. The folder will be created if it does not exist. |
| `metadata.description` | body | `string` | no | Optional text used for indexing the document. |
| `metadata.tags[]` | body | `array<string>` | no | Optional tags for the document. Send multiple values as a array. |
| `metadata.archiveDuration` | body | `number` | no | Optional archiving duration in milliseconds; empty archives forever. |
| `metadata.searchAttributes[]` | body | `array<object>` | no | Optional array of search attribute objects. |
