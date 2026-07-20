# Create Session with Cryptolens

Creates a payment form session in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/paymentform/CreateSession`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Create Session](https://app.cryptolens.io/docs/api/v3/PFCreateSession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PaymentFormId` | query | `number` | yes | The payment form id. |
| `Currency` | query | `string` | yes | The currency. |
| `Expires` | query | `string` | yes | The expiration time. |
