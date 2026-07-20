# Create Customer Charge with Saastic

Creates a customer charge in Saastic.

## Endpoint

- **Method:** `POST`
- **Path:** `/beacon/charges`
- **Base URL:** `https://api.moregoodreviews.com`
- **Official documentation:** [Create Customer Charge](https://docs.moregoodreviews.com/platform/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The customer's email address. Required when phone is not provided. |
| `phone` | body | `string` | no | The customer's phone number. Required when email is not provided. |
| `amount` | body | `number` | no | Amount of charge in the lowest currency denomination. |
| `currency` | body | `string` | no | The 3-letter currency code. |
| `location_slug` | body | `string` | no | The slug of a location. If provided, the default location for the customer will be changed to this one. |
| `charged_at` | body | `date` | no | The date the customer was charged. |
