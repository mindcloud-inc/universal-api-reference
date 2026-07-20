# Update User with SimpliRoute

Updates an existing driver in SimpliRoute.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/accounts/drivers/:user_id/`
- **Base URL:** `https://api.simpliroute.com`
- **Official documentation:** [Update User](https://documentation.simpliroute.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Optional email address for the driver. |
| `is_admin` | body | `boolean` | no | Set true to give the driver admin access. |
| `name` | body | `string` | yes | Updated display name for the driver. |
| `password` | body | `string` | yes | Password to keep or replace on the driver account. |
| `user_id` | path | `number` | yes | The SimpliRoute driver ID. |
| `username` | body | `string` | yes | Updated username for the driver. |
