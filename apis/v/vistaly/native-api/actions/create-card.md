# Create Card with Vistaly

Creates a new card in Vistaly.

## Endpoint

- **Method:** `POST`
- **Path:** `/beta/cards`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Create Card](https://docs.vistaly.com/api-reference/cards/create-a-new-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardTitle` | body | `string` | yes | The title of the card. |
| `parentId` | body | `string` | yes | The ID of the parent to associate with this card. |
| `parentType` | body | `list` | yes | The type of the parent. Accepted values: `backlog`, `card`. |
| `cardDetails` | body | `string` | no | The detailed description of the card. |
| `cardStatus` | body | `list` | no | The initial status of the card. Accepted values: `addressed`, `at risk`, `developing`, `done`, `failed`, `idea`, `identified`, `later`, `next`, `not now`, `now`, `on track`, `passed`, `pending`, `progressing`, `running`, `uncommitted`. |
| `cardType` | body | `list` | no | The type of card to create. Accepted values: `assumption`, `experiment`, `kpi`, `objective`, `opportunity`, `outcome`, `problem`, `product`, `solution`. |
| `resources[]` | body | `array<object>` | no | Optional resource links associated with the card. |
