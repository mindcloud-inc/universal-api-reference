# Top Up Gift Card with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/gift-cards/:code/top-up`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Top Up Gift Card](https://developer.giftup.com/api#top-up-a-gift-card)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | path | `string` | yes |
| `amount` | body | `number` | no |
| `units` | body | `number` | no |
| `reason` | body | `string` | no |
| `locationId` | body | `string` | no |
| `metadata` | body | `object` | no |
