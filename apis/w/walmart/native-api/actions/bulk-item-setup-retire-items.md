# Bulk Item Setup - Retire Items with Walmart

Permanently retire a list of Items identified by their SKU.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Item Setup - Retire Items](https://developer.walmart.com/us-marketplace/reference/itembulkuploads#:~:text=Utilities-,Bulk%20Item%20Setup%20%28Multiple%29,-POST)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no | — |
| `items[].sku` | body | `string` | no | The SKU to retire. |
