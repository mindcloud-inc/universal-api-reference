# Update Customer with Cratejoy

Updates an existing customer in Cratejoy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/customers/:customerId/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Update Customer](https://docs.cratejoy.com/reference/methods-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | The Cratejoy customer ID. |
| `first_name` | body | `string` | no | The customer's first name. |
| `last_name` | body | `string` | no | The customer's last name. |
| `email` | body | `string` | no | The customer's email address. |
| `note` | body | `string` | no | A note to prepend to the customer's existing note. |
