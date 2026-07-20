# Add Coupon with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/form/coupon`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Add Coupon](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `element` | body | `string` | yes | ID of the payment element to which the coupon is added. |
| `name` | body | `string` | yes | Name of the coupon. |
| `code` | body | `string` | yes | Coupon code. |
| `couponLimit` | body | `number` | yes | Maximum number of times the coupon can be used. |
| `limitDate` | body | `string` | yes | Date and time limit for the coupon. |
| `limitValue` | body | `number` | yes | Minimum value required to apply the coupon. |
| `type` | body | `string` | yes | Type of discount. |
| `discountRate` | body | `number` | yes | Discount rate (percentage). |
| `discountAmt` | body | `number` | yes | Discount amount (fixed). |
| `applyTo` | body | `string` | yes | Specifies if the coupon applies to all products or specific products. |
