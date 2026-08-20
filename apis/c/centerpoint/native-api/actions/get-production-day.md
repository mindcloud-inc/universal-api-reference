# Get Production Day with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `production_days/:PRODUCTION_DAYS_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Production Day](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_days/PRODUCTION_DAYS_IDGET)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PRODUCTION_DAYS_ID` | path | `number` | yes |
| `fields[productions]` | query | `string` | no |
| `fields[divisions]` | query | `string` | no |
| `fields[assignedProductionTaskCategories]` | query | `string` | no |
| `fields[productionDays]` | query | `string` | no |
| `include` | query | `string` | no |
