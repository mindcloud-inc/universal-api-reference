# Create Customer with ChargeBee

Creates a new customer in ChargeBee.

## Endpoint

- **Method:** `POST`
- **Path:** `customers`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [Create Customer](https://apidocs.chargebee.com/docs/api/customers/create-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Optional ID for the new customer. If omitted, Chargebee generates one. |
| `first_name` | body | `string` | no | Customer first name. |
| `last_name` | body | `string` | no | Customer last name. |
| `email` | body | `string` | no | Customer email address. |
| `company` | body | `string` | no | Customer company name. |
