# Create Payment Link with Bridge

Creates a payment link in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/payment-links`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Payment Link](https://docs.bridgeapi.io/reference/createpaymentlink)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user.first_name` | body | `string` | no | Mandatory with lastname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.last_name` | body | `string` | no | Mandatory with firstname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.company_name` | body | `string` | no | Mandatory or firstname and last_name must be completed (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.email` | body | `string` | no | Mandatory depending on your use case |
| `user.external_reference` | body | `string` | no | We recommend filling this value with a unique ID that identifies your user.  It helps Bridge optimize fraud detection by tracking how many payments have been initiated by a single user within a specific period. |
| `expired_date` | body | `date` | no | The link status will be set to "EXPIRED" after this date. Format is yyyy-MM-ddThh:mm:ssZ (ISO8601) |
| `client_reference` | body | `string` | no | A reference to link this link to your system (100 char. max) |
| `transactions[]` | body | `array<object>` | yes | Details of the payment |
| `transactions[]` | body | `array<object>` | yes | Details of the payment |
| `callback_url` | body | `string` | no | If you want to redirect the users to your interface instead of Bridge's interface  after they completed the journey from their bank website or application |
| `country` | body | `string` | no | To define the default banks displayed in the banks list. If not defined, french banks will be displayed. |
| `provider_id` | body | `number` | no | If the parameter is set, your user won't see the providers list.  Be careful to select providers with at least the single_payment capability |
