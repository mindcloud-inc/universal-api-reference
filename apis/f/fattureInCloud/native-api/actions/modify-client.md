# Modify Client with Fatture in Cloud

Updates an existing client in Fatture in Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/c/:company_id/entities/clients/:client_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Modify Client](https://developers.fattureincloud.it/api-reference/#operation/modifyClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `client_id` | path | `number` | yes | The ID of the client. |
| `data` | body | `object` | yes | The client payload inside the provider data envelope. |
