# Create Received Document with Fatture in Cloud

Creates a new received document in Fatture in Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/received_documents`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Create Received Document](https://developers.fattureincloud.it/api-reference/#operation/createReceivedDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `data` | body | `object` | yes | The received document payload inside the provider data envelope. |
