# Create Coupon Group with ReferralHero

Creates a coupon group in ReferralHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:uuid/coupon_groups`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Create Coupon Group](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#create-coupon-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | Whether the coupon group is active. |
| `coupons[]` | body | `array<string>` | no | Coupon codes to include in the group. Send multiple values as a array. |
| `name` | body | `string` | yes | Coupon group name. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
