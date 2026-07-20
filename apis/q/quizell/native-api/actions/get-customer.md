# Get Customer with Quizell

Retrieves a customer from Quizell by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/detail/:lead_id`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Get Customer](https://docs.quizell.com/customer-apis#get-customer-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The ID of the customer or lead to retrieve. |
