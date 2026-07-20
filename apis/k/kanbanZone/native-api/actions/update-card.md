# Update Card with Kanban Zone

Updates an existing card in Kanban Zone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/cards/:id`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Update Card](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The number of the card to update |
| `title` | body | `string` | yes | Card title |
| `board` | body | `string` | no | Board public ID for the mirror card to update |
| `columnId` | body | `string` | no | Column ID for the card |
| `description` | body | `string` | no | Card description |
| `templateId` | body | `string` | no | Card template public ID |
| `blocked` | body | `boolean` | no | Blocked state for the card |
| `blockedBy` | body | `string` | no | Email of the member blocking the card |
| `blockedReason` | body | `string` | no | Blocked reason for the card |
| `dueAt` | body | `string` | no | Due date for the card |
| `owner` | body | `string` | no | Owner email for the card |
| `label` | body | `string` | no | Label name for the card |
| `watchers` | body | `list<string>` | no | Watcher email list |
| `customFields[].label` | body | `string` | no | Custom field label |
| `customFields[].value` | body | `string` | no | Custom field value |
| `links.add[].card` | body | `number` | no | Card number to link to |
| `links.add[].type` | body | `string` | no | Relationship type for links to add |
| `links.add[].url` | body | `string` | no | External URL to link to |
| `links.add[].title` | body | `string` | no | Title for the external link |
| `links.remove[].card` | body | `number` | no | Card number of the link to remove |
| `links.remove[].url` | body | `string` | no | External URL of the link to remove |
