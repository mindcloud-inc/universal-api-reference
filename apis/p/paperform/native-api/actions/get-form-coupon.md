# Get Form Coupon with Paperform

Retrieves a coupon from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/coupons/:code`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [Get Form Coupon](https://paperform.readme.io/reference/getformcoupon)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes |
| `code` | path | `string` | yes |
