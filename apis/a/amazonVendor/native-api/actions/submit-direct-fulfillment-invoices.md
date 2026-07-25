# Submit Direct Fulfillment Invoices with Amazon Vendor

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/directFulfillment/payments/v1/invoices`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Submit Direct Fulfillment Invoices](https://developer-docs.amazon.com/sp-api/reference/submitinvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoices[]` | body | `array<object>` | yes | Array of Direct Fulfillment invoice objects to submit. |
