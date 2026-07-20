# Search Cards with Placker

## Endpoint

- **Method:** `GET`
- **Path:** `/card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Search Cards](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Filter cards by title. |
| `limit` | query | `number` | no | Maximum number of cards to return. |
| `list_id` | query | `number` | no | Filter by list ID. |
| `board_id` | query | `number` | no | Filter by board ID. |
| `statuses` | query | `string` | no | Filter by card statuses. |
| `members` | query | `string` | no | Filter by member IDs. |
| `assignedToMe` | query | `boolean` | no | Return cards assigned to the current user. |
| `includeArchived` | query | `boolean` | no | Include archived cards in results. |
| `attributes` | query | `string` | no | Attribute filters. |
