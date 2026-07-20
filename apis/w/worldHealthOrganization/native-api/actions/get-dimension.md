# Get Dimension with World Health Organization

Retrieves a dimension from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/DIMENSION/:dimensionCode`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [Get Dimension](https://www.who.int/data/gho/info/gho-odata-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimensionCode` | path | `string` | yes | WHO dimension code, such as REGION, COUNTRY, SEX, AGEGROUP, or WORLDBANKINCOMEGROUP. |
