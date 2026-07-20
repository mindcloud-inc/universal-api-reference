# Update Customer with Housecall Pro

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:customer_id`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Update Customer](https://docs.housecallpro.com/docs/housecall-public-api/b1c3acd657849-update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | ID of the customer to update. |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `notifications_enabled` | body | `boolean` | no | — |
| `mobile_number` | body | `string` | no | — |
| `home_number` | body | `string` | no | — |
| `work_number` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `lead_source` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
