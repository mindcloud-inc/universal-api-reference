# Search Universal Companies with RocketReach

Finds companies in RocketReach Universal search.

## Endpoint

- **Method:** `POST`
- **Path:** `/universal/company/search`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Search Universal Companies](https://docs.rocketreach.co/reference/create_universal_company_search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `number` | no | Paginate through search results by returning results starting from this value, counting from 1. |
| `page_size` | body | `number` | no | Maximum number of search results to return per page. |
| `order_by` | body | `string` | no | Specifies the ordering of search results. Allowed values: relevance, popularity, score. |
| `query` | body | `object` | no | RocketReach universal company search filter object. Supply the exact documented filter keys inside this object. |
