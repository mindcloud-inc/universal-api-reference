# List Coupons with ReferralHero

Retrieves coupons from a coupon group in ReferralHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/coupon_groups/:id`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [List Coupons](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-coupon-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Coupon group ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
