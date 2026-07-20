# Update Organization with Agendor

Updates an existing organization in Agendor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:id`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [Update Organization](https://api.agendor.com.br/docs/#operation/Update%20organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the organization to update. |
| `organization` | body | `object` | yes | Organization payload matching Agendor's update organization body. |
