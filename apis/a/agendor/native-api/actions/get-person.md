# Get Person with Agendor

Retrieves a person from Agendor by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/:id`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [Get Person](https://api.agendor.com.br/docs/#operation/Get%20person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the person to retrieve. |
| `withCustomFields` | query | `boolean` | no | Include custom fields in the response. |
