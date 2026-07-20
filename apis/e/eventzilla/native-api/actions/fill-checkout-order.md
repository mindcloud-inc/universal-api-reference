# Fill Checkout Order with Eventzilla

Updates checkout order details in Eventzilla.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkout/fillorder`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Fill Checkout Order](https://developer.eventzilla.net/docs/#fill)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventid` | body | `number` | yes |
| `eventdateid` | body | `number` | yes |
| `checkout_id` | body | `number` | yes |
| `buyerdetails[]` | body | `array<object>` | yes |
| `tickets[]` | body | `array<object>` | yes |
| `payment_id` | body | `number` | yes |
