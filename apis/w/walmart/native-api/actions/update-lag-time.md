# Update Lag Time with Walmart

Update of lag time for items in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Update Lag Time](https://developer.walmart.com/us-marketplace/reference/updatelagtimebulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lagTime[].additionalAttributes[].name` | body | `string` | no | — |
| `lagTime[].sku` | body | `string` | no | A seller-provided Product ID. |
| `lagTimeHeader.version` | body | `string` | no | — |
| `lagTime[].additionalAttributes[].value` | body | `string` | no | — |
| `lagTime[].fulfillmentLagTime` | body | `number` | no | The # of days between when the item is ordered and when it is shipped. |
| `lagTimeHeader.feedDate` | body | `string` | no | — |
| `lagTime[].additionalAttributes[]` | body | `array` | no | — |
| `lagTime[]` | body | `array<object>` | no | — |
