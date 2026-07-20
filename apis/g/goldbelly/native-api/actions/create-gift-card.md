# Create Gift Card with Goldbelly

## Endpoint

- **Method:** `POST`
- **Path:** `gift_cards`
- **Base URL:** `https://api.goldbelly.com/v1/`
- **Official documentation:** [Create Gift Card](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#gift_cards_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Gift card amount to create. |
| `recipient_email` | body | `string` | no | Email address for the gift card recipient. |
| `message` | body | `string` | no | Optional message to include with the gift card. |
