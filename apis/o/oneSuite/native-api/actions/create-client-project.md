# Create Client Project with OneSuite

Creates a project for a client in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/clients/:client_id/projects`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Create Client Project](https://rest-api.onesuite.io/#create-client-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The ID of the client |
| `name` | body | `string` | yes | Project name |
