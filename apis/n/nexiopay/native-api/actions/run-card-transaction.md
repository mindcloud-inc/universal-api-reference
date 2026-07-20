# Run card transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/process`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Run card transaction](https://docs.nexiopay.com/reference/runcardtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Card transaction and customer data object documented by Nexio. |
| `processingOptions` | body | `object` | yes | Processing options object documented by Nexio. |
| `card` | body | `object` | no | Card information object documented by Nexio. |
| `tokenex` | body | `object` | no | TokenEx payment token object documented by Nexio. |
| `recurringId` | body | `string` | no | Recurring payment token or recurring ID documented by Nexio. |
| `terminal` | body | `object` | no | Terminal transaction object documented by Nexio. |
| `clientIp` | body | `string` | no | Client IP address for the request. |
| `isAuthOnly` | body | `boolean` | no | Whether to run an auth-only transaction. |
| `paymentMethod` | body | `string` | no | Payment method selector documented by Nexio. |
| `external3ds` | body | `object` | no | External 3DS data object documented by Nexio. |
| `installment` | body | `object` | no | Installment data object documented by Nexio. |
