# Delete Issued Document with Fatture in Cloud

Deletes an existing issued document from Fatture in Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/c/:company_id/issued_documents/:document_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Delete Issued Document](https://developers.fattureincloud.it/api-reference/#operation/deleteIssuedDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `document_id` | path | `number` | yes | The ID of the document. |
