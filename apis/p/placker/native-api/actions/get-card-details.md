# Get Card Details with Placker

## Endpoint

- **Method:** `GET`
- **Path:** `/card/:card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Get Card Details](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Card ID. |
| `attributes` | query | `string` | no | Comma-separated attribute names to include. |
