# Get Card Context with Vistaly

Retrieves card context from Vistaly.

## Endpoint

- **Method:** `GET`
- **Path:** `/beta/cards/{cardId}/context`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Get Card Context](https://docs.vistaly.com/api-reference/cards/get-card-context)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The unique identifier for the card. |
| `direction` | query | `list` | no | Direction to traverse the card hierarchy. Accepted values: `ancestors`, `both`, `descendants`. |
| `maxLevels` | query | `number` | no | Maximum hierarchy depth to traverse. |
| `includeTargetCard` | query | `boolean` | no | Include the target card in results. |
| `includeComments` | query | `boolean` | no | Include comments for each card. |
| `includeInsights` | query | `boolean` | no | Include insights for each card. |
| `includeDescriptions` | query | `boolean` | no | Include card descriptions. |
