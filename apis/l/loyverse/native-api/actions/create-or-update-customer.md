# Create or Update Customer with Loyverse

Creates or updates a customer in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Create or Update Customer](https://developer.loyverse.com/docs/#tag/Customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | The customer id. If included in the POST request it will cause an update instead of a creating a new object. |
| `name` | body | `string` | yes | The customer's name |
| `email` | body | `string` | no | The customer's email |
| `phone_number` | body | `string` | no | The customer's phone number |
| `address` | body | `string` | no | The customer's address |
| `city` | body | `string` | no | The customer's city, town, or village. |
| `region` | body | `string` | no | The customer’s region name. Typically a province, a state, or a prefecture. |
| `postal_code` | body | `string` | no | The customer’s postal code, also known as zip, postcode, Eircode, etc. |
| `country_code` | body | `string` | no | The two-letter country code corresponding to the customer's country in ISO 3166-1-alpha-2 format. |
| `customer_code` | body | `string` | no | — |
| `note` | body | `string` | no | The note about the customer |
| `first_visit` | body | `date` | no | The date of the first customer visit |
| `last_visit` | body | `date` | no | The date of the most recent customer visit |
| `total_visits` | body | `number` | no | The total number of visits |
| `total_spent` | body | `number` | no | The total money amount that customer had spent |
| `total_points` | body | `number` | no | Actual customer points balance |
| `created_at` | body | `date` | no | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `updated_at` | body | `date` | no | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `deleted_at` | body | `date` | no | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `permanent_deletion_at` | body | `date` | no | The time when the customer data will be permanently deleted (usually 24 hours after soft deletion) |
