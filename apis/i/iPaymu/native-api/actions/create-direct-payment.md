# Create Direct Payment with iPaymu

Create a direct payment and return the payment details for the selected channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/direct`
- **Base URL:** `https://my.ipaymu.com/api/v2`
- **Official documentation:** [Create Direct Payment](https://ipaymu.com/api-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Customer name. |
| `phone` | body | `string` | yes | Customer phone number. |
| `email` | body | `string` | yes | Customer email address. |
| `amount` | body | `number` | yes | Payment amount. |
| `notifyUrl` | body | `string` | yes | Callback URL for payment updates. |
| `referenceId` | body | `string` | yes | Merchant reference for the payment. |
| `paymentMethod` | body | `string` | yes | Payment method code, for example va. |
| `paymentChannel` | body | `string` | yes | Payment channel code, for example bca. |
