# Create Card with vPlan

## Endpoint

- **Method:** `POST`
- **Path:** `/collection/[:collection_id]/card`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Create Card](https://docs.api.vplan.com/card.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | — |
| `description` | body | `string` | no | Card description. |
| `name` | body | `string` | yes | Card name. |
