# List Seller Items_v2 with eBay

Retrieve items listed by the authenticated user, including item data.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.ebay.com/ws/api.dll`
- **API:** REST eBay XML
- **Official documentation:** [List Seller Items_v2](https://developer.ebay.com/devzone/xml/docs/reference/ebay/GetSellerList.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startTimeTo` | body | `date` | no | — |
| `startTimeFrom` | body | `date` | no | — |
| `skus` | body | `string` | no | (SKUArray) Send multiple values as a array. |
