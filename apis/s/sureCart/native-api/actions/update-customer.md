# Update Customer with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/customers/:id`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Customer](https://developer.surecart.com/api-reference/customers/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The customer ID to update. |
| `customer.name` | body | `string` | no | The updated customer full name or business name. |
| `cascade_default_payment_method` | query | `boolean` | no | Cascade the default payment method to all subscriptions for this customer. |
