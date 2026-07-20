# List Coupons with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/coupons`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Coupons](https://runsignup.com/API/race/:race_id/coupons/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
| `coupon_code` | query | `string` | no | Search by coupon code. |
| `currently_available_only` | query | `string` | no | Only include coupons that are currently available based on date. |
| `created_since` | query | `string` | no | Searches for coupons created since the given date. |
| `created_on_or_before` | query | `string` | no | Searches for coupons created on or before the given date. |
