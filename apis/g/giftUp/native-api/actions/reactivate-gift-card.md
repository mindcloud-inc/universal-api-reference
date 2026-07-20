# Reactivate Gift Card with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/gift-cards/:code/reactivate`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Reactivate Gift Card](https://developer.giftup.com/api#reactivate-a-gift-card)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | path | `string` | yes |
| `reason` | body | `string` | no |
| `locationId` | body | `string` | no |
| `metadata` | body | `object` | no |
