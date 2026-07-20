# Change Content Item Assignees And Due Dates with EasyContent

Updates assignees or due dates for an EasyContent item.

## Endpoint

- **Method:** `POST`
- **Path:** `/zapier/actions/create/change_item_assignees_and_due_dates`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [Change Content Item Assignees And Due Dates](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | body | `number` | yes |
| `articleId` | body | `number` | yes |
| `statusId` | body | `number` | yes |
| `userIds` | body | `list<number>` | no |
| `dueDate` | body | `date` | no |
