# Add Cards with Kanban Zone

Creates cards in Kanban Zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Add Cards](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | body | `string` | yes | Board public ID for the cards to add |
| `addToTop` | body | `boolean` | no | Whether to add cards to the top of the target column |
| `cards[].title` | body | `string` | yes | Title for each card in the cards array |
| `cards[].columnId` | body | `string` | no | Column ID for each card |
| `cards[].description` | body | `string` | no | Description for each card |
| `cards[].templateId` | body | `string` | no | Card template public ID for each card |
| `cards[].blocked` | body | `boolean` | no | Blocked state for each card |
| `cards[].blockedBy` | body | `string` | no | Email of the member blocking the card |
| `cards[].blockedReason` | body | `string` | no | Blocked reason for each card |
| `cards[].dueAt` | body | `string` | no | Due date for each card |
| `cards[].owner` | body | `string` | no | Owner email for each card |
| `cards[].label` | body | `string` | no | Label name for each card |
| `cards[].watchers` | body | `list<string>` | no | Watcher email list for each card |
| `cards[].customFields[].label` | body | `string` | no | Custom field label for each card |
| `cards[].customFields[].value` | body | `string` | no | Custom field value for each card |
| `cards[].links.add[].card` | body | `number` | no | Card number to link to |
| `cards[].links.add[].type` | body | `string` | no | Relationship type for links to add |
| `cards[].links.add[].url` | body | `string` | no | External URL to link to |
| `cards[].links.add[].title` | body | `string` | no | Title for the external link |
| `cards[].links.remove[].card` | body | `number` | no | Card number of the link to remove |
| `cards[].links.remove[].url` | body | `string` | no | External URL of the link to remove |
