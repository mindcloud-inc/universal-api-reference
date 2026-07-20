# Redeem Gift Card with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/gift-cards/:code/redeem`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Redeem Gift Card](https://developer.giftup.com/api#redeem-a-gift-card)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | path | `string` | yes |
| `amount` | body | `number` | no |
| `units` | body | `number` | no |
| `reason` | body | `string` | no |
| `locationId` | body | `string` | no |
| `metadata` | body | `object` | no |
