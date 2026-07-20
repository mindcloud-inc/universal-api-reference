# Update Customer with GoTeamup

Updates an existing customer in GoTeamup.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/:id`
- **Base URL:** `https://goteamup.com/api/v2`
- **Official documentation:** [Update Customer](https://docs.goteamup.com/api-reference/endpoints/customers-partial-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | Updated customer first name |
| `id` | path | `number` | yes | The TeamUp customer ID |
| `last_name` | body | `string` | no | Customer last name. |
| `visibility` | body | `string` | no | Customer visibility status. |
| `status` | body | `string` | no | Customer status. |
| `is_status_locked` | body | `boolean` | no | Whether the customer status is locked. |
