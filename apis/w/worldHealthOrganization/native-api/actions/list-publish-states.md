# List Publish States with World Health Organization

Retrieves publish states from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/DIMENSION/PUBLISHSTATE/DimensionValues`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List Publish States](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData $filter expression for publish state values. |
