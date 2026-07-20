# Activate Offer on Card with Fidel API

Activates an offer on a Fidel card.

## Endpoint

- **Method:** `POST`
- **Path:** `/offers/:offerId/cards/:cardId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Activate Offer on Card](https://reference.fidel.uk/reference/activate-offer-on-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offerId` | path | `string` | yes | Id of the offer. |
| `cardId` | path | `string` | yes | — |
