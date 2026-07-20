# Update Client with ProProfs Project

Updates an existing client in ProProfs Project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/{{client_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Client](https://help.proprofsproject.com/clients-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The client ID to update. |
| `client_name` | body | `string` | no | The updated client name. |
