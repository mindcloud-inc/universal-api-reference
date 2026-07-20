# Create Client with Fatture in Cloud

Creates a new client in Fatture in Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/entities/clients`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Create Client](https://developers.fattureincloud.it/api-reference/#operation/createClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `data` | body | `object` | yes | The client payload inside the provider data envelope. |
