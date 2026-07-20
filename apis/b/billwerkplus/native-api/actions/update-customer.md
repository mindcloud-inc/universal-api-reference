# Update Customer with Billwerkplus

Updates a customer in Billwerkplus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer/:handle`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Update Customer](https://docs.frisbii.com/reference/updatecustomerjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Customer handle. |
| `email` | body | `string` | no | Updated customer email address. |
| `first_name` | body | `string` | no | Updated customer first name. |
| `last_name` | body | `string` | no | Updated customer last name. |
| `company` | body | `string` | no | Updated customer company name. |
