# Full Text Search Austria with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/at/FullTextSearch`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [Full Text Search Austria](https://www.openplzapi.org/en/austria/#requesting-streets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchTerm` | query | `string` | yes | Street name, postal code, or locality text to search for in Austria. |
