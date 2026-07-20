# Add Card Comment with Placker

## Endpoint

- **Method:** `PUT`
- **Path:** `/card/:card/comment`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Add Card Comment](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Card ID. |
| `content` | body | `string` | yes | Comment content. |
