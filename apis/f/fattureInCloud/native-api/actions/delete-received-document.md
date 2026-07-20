# Delete Received Document with Fatture in Cloud

Deletes an existing received document from Fatture in Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/c/:company_id/received_documents/:document_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Delete Received Document](https://developers.fattureincloud.it/api-reference/#operation/deleteReceivedDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `document_id` | path | `number` | yes | The ID of the document. |
