# Create Customer with Billwerkplus

Creates a customer in Billwerkplus.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Create Customer](https://docs.frisbii.com/reference/createcustomerjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | body | `string` | yes | Per-account unique customer handle. |
| `email` | body | `string` | no | Customer email address. |
| `first_name` | body | `string` | no | Customer first name. |
| `last_name` | body | `string` | no | Customer last name. |
| `country` | body | `string` | no | Customer country as ISO 3166-1 alpha-2. |
| `test` | body | `boolean` | no | Create the customer in test mode. |
