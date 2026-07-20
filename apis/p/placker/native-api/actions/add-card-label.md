# Add Card Label with Placker

## Endpoint

- **Method:** `PUT`
- **Path:** `/card/:card/label`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Add Card Label](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Card ID. |
| `label.id` | body | `string` | yes | Label ID to add. Use the board label ID. |
