# Update Task with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Update Task](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | Id for the Endear GraphQL operation. |
| `variables.editorId` | body | `string` | yes | Editor Id for the Endear GraphQL operation. |
| `variables.title` | body | `string` | no | Title for the Endear GraphQL operation. |
| `variables.description` | body | `string` | no | Description for the Endear GraphQL operation. |
| `variables.tags[]` | body | `array<string>` | no | Tags for the Endear GraphQL operation. |
| `variables.timeZone` | body | `string` | no | Time Zone for the Endear GraphQL operation. |
| `variables.deadline` | body | `object` | no | Deadline for the Endear GraphQL operation. |
| `variables.repeat` | body | `object` | no | Repeat for the Endear GraphQL operation. |
| `variables.assigneeIds[]` | body | `array<string>` | no | Assignee Ids for the Endear GraphQL operation. |
| `variables.notifyAssignees` | body | `boolean` | no | Notify Assignees for the Endear GraphQL operation. |
| `variables.completed` | body | `boolean` | no | Completed for the Endear GraphQL operation. |
