# List Filters with TrueMail

Retrieves saved blocklist filters from TrueMail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/filters`
- **Base URL:** `https://api.mailcop.net`
- **Official documentation:** [List Filters](https://mailcop.net/docs/api-filters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_type` | query | `string` | no | Optional filter category to return. Accepted values: `0`, `1`, `2`. |
| `page` | query | `number` | no | The result page to fetch. |
