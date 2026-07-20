# List Coupon Codes with GoAffPro

Retrieves assigned coupon codes from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/coupons`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Coupon Codes](https://api.goaffpro.com/docs/admin/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return coupon codes for this affiliate ID. |
| `code` | query | `string` | no | Only return coupon codes matching this code. |
| `type` | query | `string` | no | Only return coupon codes with this type. |
