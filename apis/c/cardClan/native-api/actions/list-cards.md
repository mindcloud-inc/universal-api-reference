# List Cards with CardClan

Retrieves cards from a CardClan workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/integration/cards`
- **Base URL:** `https://app.cardclan.io/api`
- **Official documentation:** [List Cards](https://docs.cardclan.io/api-reference/integration/data/get-cards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | query | `string` | yes | Workspace identifier used to retrieve cards. |
