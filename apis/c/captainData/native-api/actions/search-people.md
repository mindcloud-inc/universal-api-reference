# Search People with Captain Data

Finds people in Captain Data by Sales Navigator query.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/search`
- **Base URL:** `https://api.captaindata.com/v1`
- **Official documentation:** [Search People](https://docs.captaindata.com/v1/api/people/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Sales Navigator people search query copied from the LinkedIn search URL. |
| `cursor` | query | `string` | no | Pagination cursor from the X-Pagination-Next response header. |
| `page_size` | query | `number` | no | Captain Data fixed people-search page size. Leave at the documented default. |
