# Create Payment Request with Bridge

Creates a payment request in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/payment-requests`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Payment Request](https://docs.bridgeapi.io/reference/createpaymentrequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | yes | The user will be redirected to this URL after the payment |
| `transactions[]` | body | `array<object>` | yes | — |
| `transactions[]` | body | `array<object>` | yes | — |
| `user.first_name` | body | `string` | no | Mandatory with lastname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.last_name` | body | `string` | no | Mandatory with firstname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.company_name` | body | `string` | no | Mandatory or firstname and last_name must be completed (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.email` | body | `string` | no | Mandatory depending on your use case |
| `user.external_reference` | body | `string` | no | We recommend filling this value with a unique ID that identifies your user.  It helps Bridge optimize fraud detection by tracking how many payments have been initiated by a single user within a specific period. |
| `provider_id` | body | `number` | yes | The unique identifier of the user's provider |
