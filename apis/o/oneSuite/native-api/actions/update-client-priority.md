# Update Client Priority with OneSuite

Updates a client's priority in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/clients/:client_id/priority`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Client Priority](https://rest-api.onesuite.io/#update-client-39-s-priority-assignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The ID of the client |
| `priorityId` | body | `string` | yes | Priority ID to assign |
