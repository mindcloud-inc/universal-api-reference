# Search Walmart Catalog with Walmart

Search the Walmart.com global product catalog by item keyword, UPC or GTIN.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/items/walmart/search`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Search Walmart Catalog](https://developer.walmart.com/us-marketplace/reference/getsearchresult)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | This parameter allows you to perform a general search based on descriptive terms related to the product.  Example: `keyboard and mouse` |
| `upc` | query | `string` | no | Search by the 12-digit Universal Product Code (UPC). |
| `gtin` | query | `string` | no | Search by the 14-digit Global Trade Item Number (GTIN). |
