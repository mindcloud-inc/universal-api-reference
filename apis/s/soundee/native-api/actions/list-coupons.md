# List Coupons with Soundee

Retrieves your coupon codes from Soundee.

## Endpoint

- **Method:** `GET`
- **Path:** `/coupons`
- **Base URL:** `https://api.soundee.com/me`
- **Official documentation:** [List Coupons](https://soundee.readme.io/reference/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_type` | query | `string` | no | Filter coupons by state. |
| `q` | query | `string` | no | Search coupons by name or amount. |
