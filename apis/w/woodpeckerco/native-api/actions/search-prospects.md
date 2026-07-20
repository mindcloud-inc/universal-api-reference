# Search Prospects with Woodpecker.co

Finds prospects in Woodpecker by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1/prospects`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Search Prospects](https://developers.woodpecker.co/docs/prospects/get-search-prospects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Woodpecker search expression, for example email=test@example.com. |
