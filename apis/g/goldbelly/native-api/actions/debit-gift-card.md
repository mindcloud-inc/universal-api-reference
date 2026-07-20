# Debit Gift Card with Goldbelly

## Endpoint

- **Method:** `POST`
- **Path:** `gift_cards/:code/debits`
- **Base URL:** `https://api.goldbelly.com/v1/`
- **Official documentation:** [Debit Gift Card](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#gift_cards__code__debits_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Gift card code to debit. |
| `amount` | body | `number` | yes | Amount to debit from the gift card. |
