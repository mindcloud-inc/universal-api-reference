# Create Order with Crossmint

Creates an order in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2022-06-09/orders`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Order](https://docs.crossmint.com/api-reference/headless/create-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment.method` | body | `string` | yes | Blockchain or payment rail used to pay for the order. |
| `payment.currency` | body | `string` | yes | Currency used for payment. |
| `payment.receiptEmail` | body | `string` | yes | Email for the payment receipt. |
| `payment.payerAddress` | body | `string` | yes | Wallet address that will pay for the order. |
| `lineItems.collectionLocator` | body | `string` | yes | Collection locator for the order line item. |
| `lineItems.callData.totalPrice` | body | `string` | yes | Quoted total price for the line item. |
| `recipient.email` | body | `string` | yes | Email for the NFT recipient. |
| `locale` | body | `string` | no | Checkout locale. |
