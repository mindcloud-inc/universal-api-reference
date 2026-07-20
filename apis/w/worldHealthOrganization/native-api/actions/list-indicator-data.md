# List Indicator Data with World Health Organization

Retrieves data for an indicator from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/:indicatorCode`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List Indicator Data](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indicatorCode` | path | `string` | yes | WHO indicator code to read observations for, such as WHOSIS_000001. |
| `$filter` | query | `string` | no | Optional OData $filter expression, for example SpatialDim eq 'BRA' or TimeDim eq 2020. |
