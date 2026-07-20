# Get Customer with Mailchimp

Retrieves a customer from a Mailchimp e-commerce store.

## Endpoint

- **Method:** `GET`
- **Path:** `ecommerce/stores/:store_id/customers/:customer_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get Customer](https://mailchimp.com/developer/marketing/api/ecommerce-customers/get-customer-info/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `store_id` | path | `string` | yes | The store id. |
| `customer_id` | path | `string` | yes | The customer id. |
