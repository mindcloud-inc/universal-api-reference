# Get Organization with Agendor

Retrieves an organization from Agendor by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:id`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [Get Organization](https://api.agendor.com.br/docs/#operation/Get%20organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the organization to retrieve. |
| `withCustomFields` | query | `boolean` | no | Include custom fields in the response. |
