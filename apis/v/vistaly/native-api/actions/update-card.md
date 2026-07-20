# Update Card with Vistaly

Updates an existing card in Vistaly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/beta/cards/{cardId}`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Update Card](https://docs.vistaly.com/api-reference/cards/update-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The unique identifier for the card. |
| `cardTitle` | body | `string` | no | The updated title of the card. |
| `cardType` | body | `list` | no | The updated card type. Accepted values: `assumption`, `experiment`, `kpi`, `objective`, `opportunity`, `outcome`, `problem`, `product`, `solution`. |
| `cardDetails` | body | `string` | no | The updated detailed description of the card. |
| `cardStatus` | body | `list` | no | The updated status of the card. Accepted values: `addressed`, `at risk`, `developing`, `done`, `failed`, `idea`, `identified`, `later`, `next`, `not now`, `now`, `on track`, `passed`, `pending`, `progressing`, `running`, `uncommitted`. |
| `resources[]` | body | `array<object>` | no | Updated resource links for the card. |
