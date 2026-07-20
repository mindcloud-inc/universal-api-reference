# Update Customer with Trafft

Updates an existing customer in Trafft.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/:id`
- **Base URL:** `https://mindcloud.admin.trafft.com/api/v2`
- **Official documentation:** [Update Customer](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Trafft customer ID to update. |
| `first_name` | body | `string` | no | Customer first name. |
| `last_name` | body | `string` | no | Customer last name. |
| `email` | body | `string` | no | Customer email address. |
