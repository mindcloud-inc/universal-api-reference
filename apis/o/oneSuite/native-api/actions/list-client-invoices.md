# List Client Invoices with OneSuite

Retrieves a client's invoices from OneSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/clients/:client_id/invoices`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [List Client Invoices](https://rest-api.onesuite.io/#get-client-invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The ID of the client |
