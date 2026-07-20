# Update Current Customer with Escrow.com

Updates the current customer in Escrow.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customer/me`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Update Current Customer](https://www.escrow.com/api/docs/update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | Customer first name. |
| `last_name` | body | `string` | no | Customer last name. |
| `phone_number` | body | `string` | no | Customer phone number. |
