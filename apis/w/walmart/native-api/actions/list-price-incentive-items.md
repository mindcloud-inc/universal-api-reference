# List Price Incentive Items with Walmart

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/price/incentives`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST (nextCursor)
- **Official documentation:** [List Price Incentive Items](https://developer.walmart.com/global-marketplace/reference/getallincentives)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `incentiveStatus` | query | `list<string>` | yes |
| `incentiveType` | query | `list<string>` | no |
| `sortBy` | query | `string` | no |
| `sortOrder` | query | `string` | no |
