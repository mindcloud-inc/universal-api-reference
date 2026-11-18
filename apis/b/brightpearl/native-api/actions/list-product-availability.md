# List Product Availability with Brightpearl

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouse-service/product-availability/:productIds`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [List Product Availability](https://api-docs.brightpearl.com/warehouse/product-availability/get.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productIds` | path | `string` | yes | A single ID, comma-separated IDs, or ranges. |
| `includeOptional` | query | `list<string>` | no | Accepted values: `allocatedOrders`, `allocatedTransfers`, `breakDownByLocation`, `onOrder`. Send multiple values as a string separated by `,`. |
