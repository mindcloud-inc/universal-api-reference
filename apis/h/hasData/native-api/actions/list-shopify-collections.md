# List Shopify Collections with HasData

Retrieves Shopify collections from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/shopify/collections`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [List Shopify Collections](https://docs.hasdata.com/apis/shopify/collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of collections to retrieve. |
| `page` | query | `number` | no | Page number of collection results. |
| `url` | query | `string` | yes | Shopify store URL. |
