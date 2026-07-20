# Expire Gift with Snappy

Expires an existing unclaimed gift in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/gifts/{giftId}/expire`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Expire Gift](https://docs.snappy.com/reference/expiregift)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | query | `string` | yes |
| `giftId` | path | `string` | yes |
