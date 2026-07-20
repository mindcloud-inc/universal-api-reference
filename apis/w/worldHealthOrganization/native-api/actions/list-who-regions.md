# List WHO Regions with World Health Organization

Retrieves WHO regions from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/DIMENSION/REGION/DimensionValues`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List WHO Regions](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData $filter expression, for example Code eq 'EUR'. |
