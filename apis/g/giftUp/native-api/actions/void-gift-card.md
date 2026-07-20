# Void Gift Card with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/gift-cards/:code/void`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Void Gift Card](https://developer.giftup.com/api#void-a-gift-card)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | path | `string` | yes |
| `reason` | body | `string` | no |
| `locationId` | body | `string` | no |
| `metadata` | body | `object` | no |
