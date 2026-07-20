# Create Client with Runrun.it

Creates a new client in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Create Client](https://runrun.it/api/documentation#clients-create-a-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client.name` | body | `string` | yes | Client's name |
| `client.is_visible` | body | `boolean` | no | Client is currently visible to be used |
| `client.budgeted_hours_month` | body | `number` | no | Budgeted hours per month |
| `client.budgeted_cost_month` | body | `number` | no | Budgeted cost per month |
| `client.custom_field` | body | `string` | no | Custom field |
