# Search Tickets with Zammad

Finds tickets in Zammad by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/search`
- **Base URL:** `{baseUrl}/api/v1`
- **Official documentation:** [Search Tickets](https://docs.zammad.org/en/latest/api/intro.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query. |
