# Get Configuration by Card with CardClan

Retrieves a CardClan integration configuration for a card.

## Endpoint

- **Method:** `GET`
- **Path:** `/integration/config/by-card`
- **Base URL:** `https://app.cardclan.io/api`
- **Official documentation:** [Get Configuration by Card](https://docs.cardclan.io/examples/send-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | query | `string` | yes | Card ID used to look up the integration configuration. |
