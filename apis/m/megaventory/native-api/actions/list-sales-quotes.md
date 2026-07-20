# List Sales Quotes with Megaventory

Retrieves sales quote records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SalesQuoteGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Sales Quotes](https://api.megaventory.com/v2017a/json/metadata?op=SalesQuoteGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `mvSalesQuoteNo` | body | `string` | no | Filter results to a specific sales quote number. |
| `mvSalesQuoteStatus` | body | `string` | no | Filter results to a specific sales quote status. |
