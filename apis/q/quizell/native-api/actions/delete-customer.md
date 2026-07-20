# Delete Customer with Quizell

Deletes an existing customer from Quizell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/customers/delete/:lead_id`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Delete Customer](https://docs.quizell.com/customer-apis#delete-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The ID of the customer to delete. |
