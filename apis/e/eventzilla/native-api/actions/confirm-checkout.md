# Confirm Checkout with Eventzilla

Confirms a checkout in Eventzilla.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkout/confirm`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Confirm Checkout](https://developer.eventzilla.net/docs/#confirm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventid` | body | `number` | yes |
| `eventdateid` | body | `number` | yes |
| `checkout_id` | body | `number` | yes |
| `payment_status` | body | `string` | yes |
| `comments` | body | `string` | yes |
| `sendemail` | body | `boolean` | no |
