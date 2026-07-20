# Add Card Member with Placker

## Endpoint

- **Method:** `PUT`
- **Path:** `/card/:card/member`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Add Card Member](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Card ID. |
| `member.id` | body | `number` | yes | Member ID to add. |
