# Get Coupons with Eventix

Retrieves coupons from Eventix.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/coupon/:type`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Coupons](https://docs.weeztix.com/api/dashboard/get-coupons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `list<string>` | yes | How to handle archived Coupons. Accepted values: `0`, `1`, `2`. |
