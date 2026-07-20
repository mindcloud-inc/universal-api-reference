# Update Invoice Status with OneSuite

Updates an invoice payment status in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/invoices/:invoice_id/payment-status`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Invoice Status](https://rest-api.onesuite.io/#change-invoice-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes | Invoice ID |
