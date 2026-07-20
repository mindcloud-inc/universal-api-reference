# Create Customer with Lightspeed Retail POS (X-Series)

Creates a new customer in Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2.0/customers`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Create Customer](https://x-series-api.lightspeedhq.com/reference/createcustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | The customer's first name. |
| `last_name` | body | `string` | yes | The customer's last name. |
| `email` | body | `string` | yes | The customer's email address. |
