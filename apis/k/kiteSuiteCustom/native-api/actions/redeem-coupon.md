# Redeem Coupon with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/form/coupon/redeem`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Redeem Coupon](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `code` | body | `string` | yes | Coupon code to redeem. |
| `element` | body | `string` | yes | ID of the form element. |
