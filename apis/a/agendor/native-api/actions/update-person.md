# Update Person with Agendor

Updates an existing person in Agendor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/people/:id`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [Update Person](https://api.agendor.com.br/docs/#operation/Update%20person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the person to update. |
| `person` | body | `object` | yes | Person payload matching Agendor's update person body. |
