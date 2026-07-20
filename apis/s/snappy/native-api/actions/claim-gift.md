# Claim Gift with Snappy

Claims an existing gift in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/gifts/{giftId}/claim`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Claim Gift](https://docs.snappy.com/reference/claimgift)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | query | `string` | yes |
| `giftId` | path | `string` | yes |
| `orderRecipient` | body | `object` | yes |
| `variantId` | body | `string` | yes |
