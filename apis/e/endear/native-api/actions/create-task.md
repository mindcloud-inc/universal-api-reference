# Create Task with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Create Task](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.localId` | body | `string` | no | Local Id for the Endear GraphQL operation. |
| `variables.idempotencyKey` | body | `string` | no | Idempotency Key for the Endear GraphQL operation. |
| `variables.type` | body | `string` | yes | Type for the Endear GraphQL operation. |
| `variables.title` | body | `string` | yes | Title for the Endear GraphQL operation. |
| `variables.descriptionHtml` | body | `string` | no | Description Html for the Endear GraphQL operation. |
| `variables.timeZone` | body | `string` | yes | Time Zone for the Endear GraphQL operation. |
| `variables.dueDate` | body | `date` | yes | Due Date for the Endear GraphQL operation. |
| `variables.expiresAt` | body | `date` | no | Expires At for the Endear GraphQL operation. |
| `variables.autoAssignmentStrategy[]` | body | `array<string>` | no | Auto Assignment Strategy for the Endear GraphQL operation. |
| `variables.assignToTeamId` | body | `string` | no | Assign To Team Id for the Endear GraphQL operation. |
| `variables.assignToUserId` | body | `string` | no | Assign To User Id for the Endear GraphQL operation. |
| `variables.conditions[]` | body | `array<object>` | no | Conditions for the Endear GraphQL operation. |
| `variables.associations[]` | body | `array<object>` | no | Associations for the Endear GraphQL operation. |
| `variables.notifyAssignees` | body | `boolean` | no | Notify Assignees for the Endear GraphQL operation. |
