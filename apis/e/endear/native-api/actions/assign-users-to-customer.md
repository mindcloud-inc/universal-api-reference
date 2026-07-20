# Assign Users To Customer with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Assign Users To Customer](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.assignerId` | body | `string` | no | Assigner Id for the Endear GraphQL operation. |
| `variables.id` | body | `string` | yes | Id for the Endear GraphQL operation. |
| `variables.assigneeIds[]` | body | `array<string>` | yes | Assignee Ids for the Endear GraphQL operation. |
| `variables.skipIfCustomerAlreadyAssigned` | body | `boolean` | no | Skip If Customer Already Assigned for the Endear GraphQL operation. |
| `variables.notifyAssignees` | body | `boolean` | no | Notify Assignees for the Endear GraphQL operation. |
