# Search Contacts with CATS

Finds contacts in CATS by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/search`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Search Contacts](https://docs.catsone.com/api/v3/#contacts-search-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The string to search within contacts for. |
