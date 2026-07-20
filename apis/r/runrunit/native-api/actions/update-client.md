# Update Client with Runrun.it

Updates an existing client in Runrun.it.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/:id`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Update Client](https://runrun.it/api/documentation#clients-update-a-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
| `client.name` | body | `string` | no | Client's name |
| `client.is_visible` | body | `boolean` | no | Client is currently visible to be used |
| `client.budgeted_hours_month` | body | `number` | no | Budgeted hours per month |
| `client.budgeted_cost_month` | body | `number` | no | Budgeted cost per month |
| `client.custom_field` | body | `string` | no | Custom field |
