# Get Client with Timely

Retrieves a client from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/clients/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Get Client](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID for the client you want to retrieve |
| `id` | path | `number` | yes | Client ID to retrieve |
| `project_counts` | query | `string` | no | Specify to retrieve project counts. Example values: "true" or "false" |
