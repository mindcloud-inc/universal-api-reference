# Submit Purchase Order Acknowledgements with Amazon Vendor

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/orders/v1/acknowledgements`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Submit Purchase Order Acknowledgements](https://developer-docs.amazon.com/sp-api/reference/submitacknowledgement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acknowledgements[]` | body | `array<object>` | yes | An array of order acknowledgements to submit. |
