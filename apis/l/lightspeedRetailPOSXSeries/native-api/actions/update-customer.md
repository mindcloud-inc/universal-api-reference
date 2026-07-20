# Update Customer with Lightspeed Retail POS (X-Series)

Updates an existing customer in Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/2.0/customers/:customer_id`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Update Customer](https://x-series-api.lightspeedhq.com/reference/updatecustomerbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The customer ID to update |
| `first_name` | body | `string` | yes | Updated first name |
| `last_name` | body | `string` | yes | Updated last name |
| `email` | body | `string` | yes | Updated email address |
