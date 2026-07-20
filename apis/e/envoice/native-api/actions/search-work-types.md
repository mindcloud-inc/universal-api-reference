# Search Work Types with Envoice

Finds work types in Envoice by query.

## Endpoint

- **Method:** `GET`
- **Path:** `worktype/search`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Search Work Types](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryOptions.order` | query | `string` | no | Sort direction for work type search results. |
| `queryOptions.orderBy` | query | `string` | no | Field to order work type search results by. |
| `queryOptions.page` | query | `number` | no | Result page number. |
| `queryOptions.pageSize` | query | `number` | no | Number of results per page. |
| `queryOptions.query` | query | `string` | no | Search text for matching work types. |
