# Bulk Void Coupons with PassKit Coupons

## Endpoint

- **Method:** `DELETE`
- **Path:** `/coupon/singleUse/coupons/bulk`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Bulk Void Coupons](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classId` | body | `string` | no | Coupon campaign ID for the bulk void scope. |
| `protocol` | body | `string` | no | Pass protocol for the bulk void request. |
