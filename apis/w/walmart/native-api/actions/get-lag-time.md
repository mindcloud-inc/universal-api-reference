# Get Lag Time with Walmart

Rretrieve Lag Time for an item with a given SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/lagtime`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Lag Time](https://developer.walmart.com/us-marketplace/reference/getlagtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | query | `string` | yes | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. This will be used by the seller in the XSD file to refer to each item. |
