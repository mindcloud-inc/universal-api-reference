# Update Card with vPlan

## Endpoint

- **Method:** `PUT`
- **Path:** `/collection/[:collection_id]/card/[:card_id]`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Update Card](https://docs.api.vplan.com/card.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card_id` | path | `string` | yes | Card identifier. |
| `collection_id` | path | `string` | yes | — |
| `name` | body | `string` | no | Updated card name. |
