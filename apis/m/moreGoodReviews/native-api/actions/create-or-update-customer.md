# Create or Update Customer with More Good Reviews

Creates a customer in More Good Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/beacon/customers`
- **Base URL:** `https://api.moregoodreviews.com`
- **Official documentation:** [Create or Update Customer](https://docs.moregoodreviews.com/platform/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | The customer's first name. |
| `last_name` | body | `string` | no | The customer's last name. |
| `email` | body | `string` | no | The customer's email address. |
| `phone` | body | `string` | no | The customer's phone number. |
| `company` | body | `string` | no | The customer's company name. |
| `signed_up_at` | body | `date` | no | The date the customer signed up to your service. |
| `has_subscription` | body | `boolean` | no | Whether the customer is subscribed to your service. |
| `location_slug` | body | `string` | no | The slug of a location. |
| `notes` | body | `string` | no | Notes for internal use only. |
| `tags[]` | body | `array<string>` | no | An array of customer tag slugs to apply to the customer. |
| `address1` | body | `string` | no | The customer's address line 1. |
| `address2` | body | `string` | no | The customer's address line 2. |
| `city` | body | `string` | no | The customer's city or town. |
| `state` | body | `string` | no | The customer's state or region. |
| `postal_code` | body | `string` | no | The customer's postal code. |
