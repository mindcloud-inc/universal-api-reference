# Create Client with Paymo

Creates a client in Paymo.

## Endpoint

- **Method:** `POST`
- **Path:** `clients`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Create Client](https://github.com/paymo-org/api/blob/master/sections/clients.md#creating-a-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `name` | body | `string` | yes | The client name. |
| `email` | body | `string` | no | — |
| `email` | body | `string` | no | The client email address. |
| `phone` | body | `string` | no | — |
