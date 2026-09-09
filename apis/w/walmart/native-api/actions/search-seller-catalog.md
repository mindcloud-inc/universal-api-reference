# Search Seller Catalog with Walmart

Search your seller catalog with optional filters like Price, Listing Status, Rating etc.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/items/catalog/search`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Search Seller Catalog](https://developer.walmart.com/us-marketplace/reference/getsearchresult)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[].field` | body | `list<string>` | no | Pick a field to filter by. |
| `query` | body | `object` | no | — |
| `query.field` | body | `list<string>` | no | Choose a specific field to search. |
| `sort.field` | body | `list<string>` | no | Pick a field to sort by. |
| `filters[]` | body | `array<object>` | no | — |
| `query.value` | body | `string` | no | The value you want to search for. |
| `sort.order` | body | `list<string>` | no | Allowed: `ASC`, `DESC` |
| `filters[].op` | body | `list<string>` | no | Allowed: `equals`, `between`, `greater_than`, `less_than` |
| `sort` | body | `object` | no | Sort the results by a specific field. |
| `filters[].values` | body | `string` | no | Send multiple values as a array. |
