# Search Marketplace Email Lists with Toofr

Finds marketplace email lists in Toofr by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/search`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Search Marketplace Email Lists](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Optional provider page number. |
| `query` | query | `string` | yes | List search query. |
