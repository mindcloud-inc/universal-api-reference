# Create Demo Gift with Snappy

Creates a non-claimable demo gift in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/gifts/demo`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Create Demo Gift](https://docs.snappy.com/reference/createdemogift)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | body | `string` | yes |
| `companyId` | query | `string` | yes |
| `recipients[]` | body | `array<object>` | yes |
