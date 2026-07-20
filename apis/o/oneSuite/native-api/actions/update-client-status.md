# Update Client Status with OneSuite

Updates a client's status in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/clients/:client_id/status`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Client Status](https://rest-api.onesuite.io/#update-client-39-s-status-assignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The ID of the client |
| `statusId` | body | `string` | yes | Priority status ID to assign |
