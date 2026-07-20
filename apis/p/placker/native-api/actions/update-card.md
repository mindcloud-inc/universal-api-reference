# Update Card with Placker

## Endpoint

- **Method:** `PATCH`
- **Path:** `/card/:card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Update Card](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Card ID. |
| `title` | body | `string` | no | Updated card title. |
| `description` | body | `string` | no | Updated card description. |
| `status` | body | `string` | no | Updated card status. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
