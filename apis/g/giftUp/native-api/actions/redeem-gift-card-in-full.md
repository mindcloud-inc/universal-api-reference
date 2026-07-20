# Redeem Gift Card in Full with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/gift-cards/:code/redeem-in-full`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Redeem Gift Card in Full](https://developer.giftup.com/api#redeem-a-gift-card-in-full)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | path | `string` | yes |
| `reason` | body | `string` | no |
| `locationId` | body | `string` | no |
| `metadata` | body | `object` | no |
