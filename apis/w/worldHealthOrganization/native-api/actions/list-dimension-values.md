# List Dimension Values with World Health Organization

Retrieves values for a dimension from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/DIMENSION/:dimensionCode/DimensionValues`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List Dimension Values](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimensionCode` | path | `string` | yes | WHO dimension code, such as REGION, COUNTRY, SEX, AGEGROUP, or WORLDBANKINCOMEGROUP. |
| `$filter` | query | `string` | no | Optional OData $filter expression, for example ParentCode eq 'AMR'. |
