# Undo Gift Card Redemption with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/gift-cards/:code/undo-redemption`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Undo Gift Card Redemption](https://developer.giftup.com/api#undo-a-redemption)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | path | `string` | yes |
| `transactionId` | body | `string` | yes |
| `reason` | body | `string` | no |
| `metadata` | body | `object` | no |
