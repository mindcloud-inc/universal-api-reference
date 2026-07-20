# List Links with Rebrandly

Retrieves links from Rebrandly.

## Endpoint

- **Method:** `GET`
- **Path:** `/links`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [List Links](https://developers.rebrandly.com/docs/list-links)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of links to return. |
| `favourite` | query | `boolean` | no | Filter links by favourite status. |
| `domain.id` | query | `string` | no | Filter links by branded domain ID. |
| `domain.fullName` | query | `string` | no | Filter links by branded domain name. |
| `creator.id` | query | `string` | no | Filter links by creator ID. |
| `slashtag` | query | `string` | no | Filter links by slashtag. Requires a domain filter in Rebrandly docs. |
| `dateFrom` | query | `date` | no | Include only links created on or after this date (YYYY-MM-DD). |
| `dateTo` | query | `date` | no | Include only links created on or before this date (YYYY-MM-DD). |
| `orderBy` | query | `string` | no | Field used to sort the links collection. |
| `orderDir` | query | `string` | no | Sort direction for the links collection. |
| `last` | query | `string` | no | Cursor: the last link ID returned by the previous page. |
