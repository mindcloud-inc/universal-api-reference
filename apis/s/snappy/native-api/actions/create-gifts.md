# Create Gifts with Snappy

Creates one or more gifts in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/gifts`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Create Gifts](https://docs.snappy.com/reference/creategifts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | body | `string` | yes |
| `companyId` | query | `string` | yes |
| `recipients[]` | body | `array<object>` | yes |
