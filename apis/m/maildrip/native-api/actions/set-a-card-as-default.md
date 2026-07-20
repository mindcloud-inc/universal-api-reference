# Set a card as default with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/payment/paystack/cards/{authorization}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Set a card as default](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorization` | path | `string` | yes | The authorization code of the card to be set as default |
