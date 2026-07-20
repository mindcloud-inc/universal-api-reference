# Update Client with Paymo

Updates an existing client in Paymo.

## Endpoint

- **Method:** `PUT`
- **Path:** `clients/:clientId`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Update Client](https://github.com/paymo-org/api/blob/master/sections/clients.md#updating-a-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `number` | yes | The Paymo client ID. |
| `name` | body | `string` | no | The updated client name. |
| `email` | body | `string` | no | The updated client email address. |
| `address` | body | `string` | no | The updated client mailing address. |
