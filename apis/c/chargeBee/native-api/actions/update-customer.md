# Update Customer with ChargeBee

Updates an existing customer in ChargeBee.

## Endpoint

- **Method:** `POST`
- **Path:** `customers/:customer_id`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [Update Customer](https://apidocs.chargebee.com/docs/api/customers/update-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The unique identifier of the Chargebee customer to update. |
| `first_name` | body | `string` | no | Updated customer first name. |
| `last_name` | body | `string` | no | Updated customer last name. |
| `email` | body | `string` | no | Updated customer email address. |
