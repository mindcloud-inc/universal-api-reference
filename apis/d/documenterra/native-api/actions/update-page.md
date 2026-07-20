# Update Page with Documenterra

Updates an existing page in Documenterra.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId/articles/:topicId`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Update Page](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-obnovleniye-stranitsy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigneeUserName` | body | `string` | no | Optional updated assignee username. |
| `body` | body | `string` | no | Updated page content body. |
| `indexKeywords[]` | body | `array<string>` | no | Optional updated page index keywords. |
| `ownerUserName` | body | `string` | no | Optional updated owner username. |
| `projectId` | path | `string` | yes | Documenterra project identifier. |
| `statusName` | body | `string` | no | Optional updated Documenterra status name. |
| `title` | body | `string` | no | Updated page title. |
| `topicId` | path | `string` | yes | Documenterra page identifier. |
| `updatedFields` | body | `string` | yes | Comma-separated list of page fields to update. |
