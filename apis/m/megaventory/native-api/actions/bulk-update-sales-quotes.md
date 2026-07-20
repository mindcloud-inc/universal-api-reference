# Bulk Update Sales Quotes with Megaventory

Updates sales quotes in Megaventory in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SalesQuotesUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Bulk Update Sales Quotes](https://api.megaventory.com/v2017a/json/metadata?op=SalesQuotesUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SalesQuotes` | body | `list<object>` | yes | JSON array of sales quote objects. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
