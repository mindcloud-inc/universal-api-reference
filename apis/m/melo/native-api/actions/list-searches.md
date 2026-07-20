# List Searches with Melo

Retrieves existing searches from Melo matching the current criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/searches`
- **Base URL:** `https://preprod-api.notif.immo`
- **Official documentation:** [List Searches](https://docs.melo.io/api-reference/endpoint/searches/get_collection)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Collection page number. |
| `itemsPerPage` | query | `number` | no | Number of items per page. |
