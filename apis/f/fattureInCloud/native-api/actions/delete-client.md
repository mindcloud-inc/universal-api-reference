# Delete Client with Fatture in Cloud

Deletes an existing client from Fatture in Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/c/:company_id/entities/clients/:client_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Delete Client](https://developers.fattureincloud.it/api-reference/#operation/deleteClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `client_id` | path | `number` | yes | The ID of the client. |
