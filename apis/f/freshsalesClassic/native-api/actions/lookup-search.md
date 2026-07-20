# Lookup Search with Freshsales Classic

Finds lookup records in Freshsales Classic by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [Lookup Search](https://developers.freshworks.com/crm/api/#lookup_search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entities` | query | `string` | yes | Entity type to search, for example contact. |
| `f` | query | `string` | yes | Field to match during lookup search, for example email. |
| `q` | query | `string` | yes | Lookup text to search for. |
