# List Client Projects with OneSuite

Retrieves a client's projects from OneSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/clients/:client_id/projects`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [List Client Projects](https://rest-api.onesuite.io/#get-client-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The ID of the client |
