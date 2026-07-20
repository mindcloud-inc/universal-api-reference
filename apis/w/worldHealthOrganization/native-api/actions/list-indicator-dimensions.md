# List Indicator Dimensions with World Health Organization

Retrieves indicator dimensions from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/IndicatorDimension`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List Indicator Dimensions](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData $filter expression, for example IndicatorCode eq 'WHOSIS_000001'. |
