# Create Deal For Person with Agendor

Creates a new deal for a person in Agendor.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/:person_id/deals`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [Create Deal For Person](https://api.agendor.com.br/docs/#operation/Create%20deal%20for%20person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal` | body | `string` | yes | Deal payload as a JSON string matching Agendor's create deal for person body. |
| `person_id` | path | `number` | yes | ID of the person that will own the deal. |
