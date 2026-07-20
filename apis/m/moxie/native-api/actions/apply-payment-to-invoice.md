# Apply Payment to Invoice with Moxie

Applies a payment to an invoice in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/payment/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Apply Payment to Invoice](https://help.withmoxie.com/en/articles/8213724-apply-payment-to-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | Payment date in YYYY-MM-DD format. |
| `amount` | body | `number` | yes | Payment amount. |
| `invoiceNumber` | body | `string` | yes | Invoice number to apply the payment to. |
| `clientName` | body | `string` | no | Client name tied to the invoice. |
| `paymentType` | body | `string` | no | Optional payment type enum. Use one of OTHER, VENMO, PAYPAL, APP_PAYOUT, CREDIT_CARD, CHECK, ZELLE, STRIPE, BANK_TRANSFER, or CASH. |
| `referenceNumber` | body | `string` | no | Reference number for the payment. |
| `memo` | body | `string` | no | Internal payment memo. |
