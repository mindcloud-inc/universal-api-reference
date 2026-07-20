# Set PDF Metadata with PDF Tools by Tachytelic

## Endpoint

- **Method:** `POST`
- **Path:** `/setmetadata`
- **Base URL:** `https://pdf.tachytelic.net/api`
- **Official documentation:** [Set PDF Metadata](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#set-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PdfFileContent` | body | `string` | yes | Base64-encoded PDF content. |
| `Title` | body | `string` | no | Document title metadata to set. |
| `Author` | body | `string` | no | Document author metadata to set. |
| `Subject` | body | `string` | no | Document subject metadata to set. |
| `Keywords` | body | `string` | no | Document keywords metadata to set. |
| `CreationDate` | body | `string` | no | Document creation date metadata to set. |
| `ModificationDate` | body | `string` | no | Document modification date metadata to set. |
