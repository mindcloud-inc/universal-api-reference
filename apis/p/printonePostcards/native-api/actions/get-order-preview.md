# Get Order Preview with Print.one Postcards

Retrieves an order PDF preview from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/storage/order/preview/[:orderId]`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Get Order Preview](https://api.print.one/docs/v2#operation/Storage/getOrderPreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The ID of the order |
| `inline` | query | `boolean` | yes | Whether to render the PDF inline |
