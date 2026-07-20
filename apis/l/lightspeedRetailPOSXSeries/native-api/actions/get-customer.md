# Get Customer with Lightspeed Retail POS (X-Series)

Retrieves a customer from Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/customers/:customer_id`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Get Customer](https://x-series-api.lightspeedhq.com/reference/getcustomerbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The Lightspeed customer ID to retrieve. |
