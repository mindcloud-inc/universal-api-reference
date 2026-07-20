# Update Customer with Quizell

Updates an existing customer in Quizell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/update/:lead_id`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Update Customer](https://docs.quizell.com/customer-apis#update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_data` | body | `object` | yes | Customer data payload. |
| `lead_id` | path | `number` | yes | The ID of the customer to update. |
| `customer_custom_data` | body | `object` | no | Optional custom customer fields payload. |
