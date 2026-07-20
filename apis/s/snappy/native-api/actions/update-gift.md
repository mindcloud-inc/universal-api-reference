# Update Gift with Snappy

Updates an existing unclaimed gift in Snappy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/gifts/{giftId}`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Update Gift](https://docs.snappy.com/reference/patchgift)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | query | `string` | yes |
| `giftId` | path | `string` | yes |
