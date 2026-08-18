# Create Transaction with Centerpoint

## Endpoint

- **Method:** `POST`
- **Path:** `transactions`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Create Transaction](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/transactionsPOST)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | — |
| `data.attributes.amount` | body | `string` | no | — |
| `data.type` | body | `string` | no | transactions |
| `data.attributes` | body | `object` | no | — |
| `data.attributes.paymentMethod` | body | `string` | no | — |
| `data.attributes.notes` | body | `string` | no | — |
| `data.attributes.receivedDate` | body | `string` | no | — |
| `data.attributes.invoiceId` | body | `string` | no | — |
