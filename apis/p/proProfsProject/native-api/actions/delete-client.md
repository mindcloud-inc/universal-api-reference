# Delete Client with ProProfs Project

Deletes an existing client from ProProfs Project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/clients/{{client_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Delete Client](https://help.proprofsproject.com/clients-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The client ID to delete. |
