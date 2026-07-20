# Check number exists with Bulldog-WP

Checks whether phone numbers exist in Bulldog-WP.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/exists`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Check number exists](https://console.bulldog-wp.co.il/docs/specification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Phone number to check for WhatsApp availability. |
