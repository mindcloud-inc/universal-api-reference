# Send Document with Recommand

Sends a document through the Recommand network.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/:companyId/send`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Send Document](https://recommand.eu/en/reference/sending/send-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `doctypeId` | body | `string` | no | The document type identifier. Not required, only used when documentType is "xml". For supported document types, the doctypeId can be detected automatically from your XML document, if that's not the case you can provide it manually. |
| `document` | body | `object` | yes | document body field. |
| `documentType` | body | `string` | yes | The type of document. |
| `email` | body | `object` | no | email body field. |
| `pdfGeneration` | body | `object` | no | pdfGeneration body field. |
| `processId` | body | `string` | no | The process identifier. Not required, only used when documentType is "xml". For supported document types, the processId can be detected automatically from your XML document, if that's not the case you can provide it manually. |
| `recipient` | body | `string` | yes | The Peppol address of the recipient. If null, the document will be sent via email only (requires `email.to`). |
