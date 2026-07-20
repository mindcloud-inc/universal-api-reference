# Search Companies with Captain Data

Finds companies in Captain Data by Sales Navigator query.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/search`
- **Base URL:** `https://api.captaindata.com/v1`
- **Official documentation:** [Search Companies](https://docs.captaindata.com/v1/api/companies/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Sales Navigator company search query copied from the LinkedIn search URL. |
| `cursor` | query | `string` | no | Pagination cursor from the X-Pagination-Next response header. |
| `page_size` | query | `number` | no | Captain Data fixed company-search page size. Leave at the documented default. |
