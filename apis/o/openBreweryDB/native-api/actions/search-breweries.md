# Search Breweries with Open Brewery DB

Finds breweries in Open Brewery DB by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/breweries/search`
- **Base URL:** `https://api.openbrewerydb.org/v1`
- **Official documentation:** [Search Breweries](https://www.openbrewerydb.org/documentation#search-breweries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search term to match against brewery names. Supports partial, case-insensitive matches. |
