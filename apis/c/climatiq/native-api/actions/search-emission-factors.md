# Search Emission Factors with Climatiq

Finds emission factors in Climatiq by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/v1/search`
- **Base URL:** `https://api.climatiq.io`
- **Official documentation:** [Search Emission Factors](https://www.climatiq.io/docs/api-reference/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_version` | query | `string` | yes | Required Climatiq data version, such as ^33. |
| `query` | query | `string` | no | Free-text emission factor search query. |
| `region` | query | `string` | no | Region code filter, such as GB or US-CA. |
| `year` | query | `number` | no | Emission factor year filter. |
| `category` | query | `string` | no | Emission factor category filter. |
| `unit_type` | query | `string` | no | Unit type filter, such as Energy, Money, Weight, or Distance. |
| `scope` | query | `string` | no | GHG Protocol scope filter, such as 1, 2, 3, or 3.1. |
| `calculation_method` | query | `string` | no | Calculation method filter: ar4, ar5, or ar6. |
| `access_type` | query | `string` | no | Emission factor access type: public, private, or premium. |
| `page` | query | `number` | no | Results page number. Climatiq defaults to 1. |
| `results_per_page` | query | `number` | no | Number of results per page. Climatiq maximum is 500. |
