# Transfer Gift Card Balances with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/gift-cards/transfer-balances`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Transfer Gift Card Balances](https://developer.giftup.com/api#transfer-balances-between-gift-cards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceGiftCards[]` | body | `array<string>` | yes | Gift card codes to transfer balances from. |
| `sourceGiftCards[]` | body | `array<string>` | yes | Gift card codes to transfer balances from. |
| `sourceGiftCards[]` | body | `array<string>` | yes | Gift card codes to transfer balances from. |
| `destinationGiftCard` | body | `string` | yes | — |
| `reason` | body | `string` | no | — |
| `locationId` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
