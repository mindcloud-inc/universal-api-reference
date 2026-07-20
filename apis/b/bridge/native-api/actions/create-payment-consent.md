# Create Payment Consent with Bridge

Creates a payment consent in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/consents`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Payment Consent](https://docs.bridgeapi.io/reference/createpaymentconsent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_reference` | body | `string` | yes | A reference to your payment |
| `redirect_url` | body | `string` | yes | URL to redirect the user after consent completion |
| `transactions[]` | body | `array<object>` | yes | Details of the payment that requires consent |
| `transactions[]` | body | `array<object>` | yes | Details of the payment that requires consent |
| `user.first_name` | body | `string` | no | Mandatory with lastname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.last_name` | body | `string` | no | Mandatory with firstname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.company_name` | body | `string` | no | Mandatory or firstname and last_name must be completed (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.email` | body | `string` | yes | Mandatory |
