# Domain Search with Tomba

Finds contacts in Tomba by domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain-search`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Domain Search](https://docs.tomba.io/api/finder#domain-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to search for company contacts. |
| `company` | query | `string` | no | Company name to search when a domain is not available. |
| `page` | query | `number` | no | Page number to retrieve. |
| `limit` | query | `string` | no | Maximum number of results to return. |
| `country` | query | `string` | no | Two-letter country code to narrow the search. |
| `department` | query | `string` | no | Department filter for returned contacts. |
