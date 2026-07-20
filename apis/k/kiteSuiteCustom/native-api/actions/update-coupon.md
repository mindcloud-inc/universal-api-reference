# Update Coupon with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/coupon/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Coupon](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the coupon to update. |
| `name` | body | `string` | yes | Name of the coupon. |
| `couponLimit` | body | `string` | yes | Limit type for the coupon. |
| `limitDate` | body | `string` | yes | Date and time limit for the coupon (if couponLimit is 'date'). |
| `limitValue` | body | `number` | yes | Maximum number of times the coupon can be used (if couponLimit is 'count'). |
| `type` | body | `string` | yes | Type of discount. |
| `discountRate` | body | `number` | yes | Discount rate (percentage). |
| `discountAmt` | body | `number` | yes | Discount amount (fixed). |
| `applyTo` | body | `string` | yes | Specifies if the coupon applies to all products or specific products. |
| `isEnable` | body | `boolean` | yes | Indicates if the coupon is enabled. |
