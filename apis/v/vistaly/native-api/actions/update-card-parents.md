# Update Card Parents with Vistaly

Updates a card's parents in Vistaly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/beta/cards/{cardId}/parents`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Update Card Parents](https://docs.vistaly.com/api-reference/cards/update-card-parents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The unique identifier for the card. |
| `add[]` | body | `array<object>` | no | Parents to add to the card. |
| `remove[]` | body | `array<object>` | no | Parents to remove from the card. |
