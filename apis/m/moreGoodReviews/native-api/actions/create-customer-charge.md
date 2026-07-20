# Create Customer Charge with More Good Reviews

Creates a customer charge in More Good Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/beacon/charges`
- **Base URL:** `https://api.moregoodreviews.com`
- **Official documentation:** [Create Customer Charge](https://docs.moregoodreviews.com/platform/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The customer's email address. |
| `phone` | body | `string` | no | The customer's phone number. |
| `amount` | body | `number` | no | Amount of charge in lowest currency denomination. |
| `currency` | body | `string` | no | The 3-letter currency code. |
| `location_slug` | body | `string` | no | The slug of a location. |
| `charged_at` | body | `date` | no | The date the customer was charged. |
