# List Production Items with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `production_items`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Production Items](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_itemsGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reports[0]` | query | `string` | no |
| `reports[1]` | query | `string` | no |
| `filter[domain]` | query | `string` | no |
| `reports[2]` | query | `string` | no |
| `filter[production]` | query | `string` | no |
| `reports[3]` | query | `string` | no |
| `include` | query | `string` | no |
| `sort` | query | `string` | no |
| `PRODUCTION_ID` | query | `string` | yes |
