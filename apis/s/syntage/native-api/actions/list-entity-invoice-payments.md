# List Entity Invoice Payments with Syntage

Retrieves invoice payments for an entity in Syntage.

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/:entityId/invoices/payments`
- **Base URL:** `https://api.sandbox.syntage.com`
- **Official documentation:** [List Entity Invoice Payments](https://docs.syntage.com/api-reference/ds-mx-sat-invoice-payments/list-taxpayers-invoice-payments.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | path | `string` | yes | The Syntage entity identifier. |
