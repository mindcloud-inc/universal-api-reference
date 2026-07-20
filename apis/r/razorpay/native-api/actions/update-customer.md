# Update Customer with Razorpay

Updates an existing customer in Razorpay.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/customers/:id`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Update Customer](https://razorpay.com/docs/api/customers/edit/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the customer. |
| `name` | body | `string` | no | — |
| `contact` | body | `string` | no | — |
| `email` | body | `string` | no | — |
