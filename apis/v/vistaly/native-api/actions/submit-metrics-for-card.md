# Submit Metrics for Card with Vistaly

Creates metrics for a card in Vistaly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/cards/{cardId}/metrics`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Submit Metrics for Card](https://docs.vistaly.com/api-reference/cards/submit-metrics-for-a-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The unique identifier for the card whose metrics are being submitted. |
| `value` | body | `number` | yes | The metric value. |
| `timestamp` | body | `date` | no | The metric timestamp. |
