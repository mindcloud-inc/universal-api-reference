# Submit Bulk Metrics for Card with Vistaly

Creates bulk metrics for a card in Vistaly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/cards/{cardId}/metrics/bulk`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Submit Bulk Metrics for Card](https://docs.vistaly.com/api-reference/cards/submit-bulk-metrics-for-a-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The unique identifier for the card whose metrics are being submitted. |
| `metrics[]` | body | `array<object>` | yes | Metric datapoints to create. |
