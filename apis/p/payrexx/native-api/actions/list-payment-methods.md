# List Payment Methods with Payrexx

Retrieves active payment methods from Payrexx.

## Endpoint

- **Method:** `GET`
- **Path:** `PaymentMethod/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [List Payment Methods](https://developers.payrexx.com/reference/get-all-active-payment-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterCurrency` | body | `string` | no | Currency to filter active payment methods by. |
| `filterPaymentType` | body | `string` | no | Payment type to filter active payment methods by. |
| `filterPsp` | body | `number` | no | PSP ID to filter active payment methods by. |
