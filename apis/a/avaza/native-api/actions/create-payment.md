# Create Payment with Avaza

Creates a new payment in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Payment`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Payment](https://api.avaza.com/#!/Payment/Payment_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Amount` | body | `number` | no | — |
| `PaymentNumber` | body | `string` | no | Optional. If not specified will be automatically generated |
| `DateIssued` | body | `date` | no | Date of Payment. If not specified, assumes today. |
| `TransactionPrefix` | body | `string` | no | Optional to override the default prefix added to Payment Numbers |
| `CustomerIDFK` | body | `number` | no | Only required if no invoice allocations specified. |
| `ExchangeRate` | body | `number` | no | Optional. Only used when the Customer's currecy is different from the Avaza account's base currency. Specifies the exchange rate that should apply between the customer currency and base currency. If not provided we will obtain an up to date exchange rate for the Payment Issue Date. |
| `TransactionReference` | body | `string` | no | Optional for storing the reference # of the payment method. |
| `Notes` | body | `string` | no | — |
| `PaymentProviderCode` | body | `string` | no | Optional for storing the payment provider who was the source of funds. |
| `PaymentAllocations` | body | `list<object>` | yes | List of amounts within this payment that are allocated to invoices. The sum of these be less than or equal to the payment amount. |
| `InvoiceTransactionIDFK` | body | `number` | no | The Avaza Invoice TransactionID that is having a payment amount allocated to it. |
| `AllocationAmount` | body | `number` | no | The Amount being allocated to the invoice. Expects same currency as invoice currency |
| `AllocationDate` | body | `date` | no | Optional. Defaults to the current time in the Avaza account's timezone. The date the allocation is applied to the invoice. Can be difference from the Payment Date when doing prepayments etc. |
