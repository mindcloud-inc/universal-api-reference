# List Income Groups with World Health Organization

Retrieves income groups from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/DIMENSION/WORLDBANKINCOMEGROUP/DimensionValues`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List Income Groups](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData $filter expression, for example Code eq 'WB_HI'. |
