# Delete Customer with Mailchimp

Deletes an existing customer from a Mailchimp e-commerce store.

## Endpoint

- **Method:** `DELETE`
- **Path:** `ecommerce/stores/:store_id/customers/:customer_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Delete Customer](https://mailchimp.com/developer/marketing/api/ecommerce-customers/delete-customer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store_id` | path | `string` | yes | The store id. |
| `customer_id` | path | `string` | yes | The customer id. |
