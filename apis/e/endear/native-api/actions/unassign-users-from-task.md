# Unassign Users From Task with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Unassign Users From Task](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | Id for the Endear GraphQL operation. |
| `variables.assignerId` | body | `string` | yes | Assigner Id for the Endear GraphQL operation. |
| `variables.assigneeIds[]` | body | `array<string>` | yes | Assignee Ids for the Endear GraphQL operation. |
