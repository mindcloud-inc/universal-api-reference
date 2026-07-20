# Create Checkout with Eventzilla

Creates a checkout in Eventzilla.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkout/create`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Create Checkout](https://developer.eventzilla.net/docs/#create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventid` | body | `number` | yes |
| `eventdateid` | body | `number` | yes |
| `ticket_types[]` | body | `array<object>` | yes |
| `discount_code` | body | `string` | no |
