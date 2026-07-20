# Update Client with OneSuite

Updates a client in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/clients/:client_id`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Client](https://rest-api.onesuite.io/#update-client-with-all-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The ID of the client to update |
| `name` | body | `string` | no | Updated client name |
