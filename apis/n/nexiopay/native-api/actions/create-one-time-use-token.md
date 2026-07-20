# Create one-time-use token with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/token`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Create one-time-use token](https://docs.nexiopay.com/reference/createonetimeusetoken-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | Transaction and customer data object documented by Nexio. |
| `card` | body | `object` | no | Card information object documented by Nexio. |
| `bank` | body | `object` | no | Bank account information object documented by Nexio. |
| `processingOptions` | body | `object` | no | Processing options object documented by Nexio. |
| `uiOptions` | body | `object` | no | Iframe UI options object documented by Nexio. |
| `paymentMethod` | body | `string` | no | Payment method selector documented by Nexio. |
| `shouldUpdateCard` | body | `boolean` | no | Whether Nexio should update an existing card token. |
| `isAuthOnly` | body | `boolean` | no | Whether to create the token for an auth-only transaction. |
| `installment` | body | `object` | no | Installment data object documented by Nexio. |
