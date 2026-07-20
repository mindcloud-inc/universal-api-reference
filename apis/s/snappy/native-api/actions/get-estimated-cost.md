# Get Estimated Cost with Snappy

Retrieves a campaign cost estimate from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{campaignId}/estimatedCost`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Get Estimated Cost](https://docs.snappy.com/reference/getestimatedcost)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `string` | yes |
| `companyId` | query | `string` | yes |
| `numberOfGifts` | query | `number` | yes |
