# List Region Countries with World Health Organization

Retrieves region-country mappings from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/RegionCountry`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [List Region Countries](https://www.who.int/data/gho/info/gho-odata-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData $filter expression, for example RegionCode eq 'AMR' or CountryCode eq 'BRA'. |
