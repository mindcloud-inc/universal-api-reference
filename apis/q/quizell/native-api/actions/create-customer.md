# Create Customer with Quizell

Creates a new customer in Quizell.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/store`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Create Customer](https://docs.quizell.com/customer-apis#create-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_data` | body | `object` | yes | Customer data payload. |
| `customer_custom_data` | body | `object` | no | Optional custom customer fields payload. |
