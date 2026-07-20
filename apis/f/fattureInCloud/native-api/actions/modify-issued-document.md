# Modify Issued Document with Fatture in Cloud

Updates an existing issued document in Fatture in Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/c/:company_id/issued_documents/:document_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Modify Issued Document](https://developers.fattureincloud.it/api-reference/#operation/modifyIssuedDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `document_id` | path | `number` | yes | The ID of the document. |
| `data` | body | `object` | yes | The issued document payload inside the provider data envelope. |
