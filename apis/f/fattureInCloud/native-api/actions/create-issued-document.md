# Create Issued Document with Fatture in Cloud

Creates a new issued document in Fatture in Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/issued_documents`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Create Issued Document](https://developers.fattureincloud.it/api-reference/#operation/createIssuedDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `data` | body | `object` | yes | The issued document payload inside the provider data envelope. |
