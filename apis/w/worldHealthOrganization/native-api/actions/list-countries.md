# List Countries with World Health Organization

Retrieves countries from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/DIMENSION/COUNTRY/DimensionValues`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List Countries](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData $filter expression, for example ParentCode eq 'AMR'. |
