# List Domains with Rebrandly

Retrieves domains from Rebrandly.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [List Domains](https://developers.rebrandly.com/docs/listing-your-domains-collection)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of domains to return. |
| `active` | query | `boolean` | no | Filter by whether the domain can currently be used to brand links. |
| `type` | query | `string` | no | Filter domains by type. |
| `orderBy` | query | `string` | no | Field used to sort the domains collection. |
| `orderDir` | query | `string` | no | Sort direction for the domains collection. |
| `last` | query | `string` | no | Cursor: the last domain ID returned by the previous page. |
