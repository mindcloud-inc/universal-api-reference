# Create User with SimpliRoute

Creates a new driver in SimpliRoute.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/drivers/`
- **Base URL:** `https://api.simpliroute.com`
- **Official documentation:** [Create User](https://documentation.simpliroute.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Optional email address for the driver. |
| `is_admin` | body | `boolean` | no | Set true to create the user as an admin. |
| `name` | body | `string` | yes | Display name for the driver. |
| `password` | body | `string` | yes | Password for the new driver. |
| `phone` | body | `string` | no | Optional phone number for the driver. |
| `username` | body | `string` | yes | Unique username for the driver. |
