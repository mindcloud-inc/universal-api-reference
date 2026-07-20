# Split PDF with Plumsail Documents

Splits a PDF in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/pdf/split`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Split PDF](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Type` | body | `string` | no |
| `ExtractRange` | body | `string` | no |
| `PagesInChunk` | body | `number` | no |
| `ChunksRange` | body | `string` | no |
| `BookmarkDepth` | body | `number` | no |
| `UseBookmarksForFileNames` | body | `boolean` | no |
| `FilenamePrefix` | body | `string` | no |
| `Password` | body | `string` | no |
| `File` | body | `file` | no |
| `FileUrl` | body | `string` | no |
| `CallbackUrl` | body | `string` | no |
