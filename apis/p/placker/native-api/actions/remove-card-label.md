# Remove Card Label with Placker

## Endpoint

- **Method:** `DELETE`
- **Path:** `/card/:card/label/:label`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Remove Card Label](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Card ID. |
| `label` | path | `string` | yes | Label ID. |
