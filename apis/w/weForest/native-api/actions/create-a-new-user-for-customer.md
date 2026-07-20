# Create a new user for customer with WeForest

Creates a new customer user in WeForest.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/:id/users`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Create a new user for customer](https://docs.weforest.org/create-a-new-user-for-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer identifier from WeForest. |
| `firstName` | body | `string` | yes | First name for the new customer user. |
| `lastName` | body | `string` | yes | Last name for the new customer user. |
| `email` | body | `string` | yes | Email for the new customer user. |
| `password` | body | `string` | yes | Password for the new customer user. |
