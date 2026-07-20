# Search Leads with Teamgate

Finds leads in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Search Leads](https://developers.teamgate.com/#1b80ca61-833a-472a-b127-e3b6d5e18902)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | no | Lead source name filter. |
| `industry` | query | `string` | no | Lead industry name filter. |
| `operator` | query | `string` | no | Logical operator for combining search conditions, such as OR. |
| `fields` | query | `string` | no | Comma-separated fields to return in the search response. |
