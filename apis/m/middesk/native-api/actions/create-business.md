# Create a business with Middesk

Creates a business in your Middesk account.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a business](https://docs.middesk.com/reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses[]` | body | `array` | yes | Addresses for the business to create. |
| `name` | body | `string` | yes | Legal or business name for the business to create. |
