# Search Tickets with Freshdesk

Finds tickets in Freshdesk by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/tickets`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Search Tickets](https://developers.freshdesk.com/api/#filter_tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Freshdesk filter query syntax, for example status:2. |
