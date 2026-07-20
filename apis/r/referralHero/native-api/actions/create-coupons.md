# Create Coupons with ReferralHero

Creates coupons in ReferralHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:uuid/coupons`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Create Coupons](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#create-coupons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coupon_group_id` | body | `string` | yes | Coupon group ID. |
| `coupons[]` | body | `array<string>` | yes | Coupon codes to add. Send multiple values as a array. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
