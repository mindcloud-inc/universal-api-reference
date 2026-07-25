# Submit Direct Fulfillment Acknowledgements with Amazon Vendor

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/directFulfillment/orders/2021-12-28/acknowledgements`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Submit Direct Fulfillment Acknowledgements](https://developer-docs.amazon.com/sp-api/reference/submitacknowledgement-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderAcknowledgements[]` | body | `array<object>` | yes | List of one or more Direct Fulfillment purchase order acknowledgements. |
