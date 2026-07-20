# Search Resources with e-Gov

Finds resources in e-Gov by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/resource_search`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Search Resources](https://data.e-gov.go.jp/data/api/3/action/help_show?name=resource_search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string` | yes |
| `order_by` | query | `string` | no |
