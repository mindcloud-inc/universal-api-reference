# Create Ticket with NeetoDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Create Ticket](https://apidocs.neetodesk.com/api-reference/tickets/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the customer. |
| `subject` | body | `string` | yes | Subject for the ticket. |
| `description` | body | `string` | yes | Description for the ticket. |
| `name` | body | `string` | no | Name of the customer. |
| `channel` | body | `string` | no | Source of the ticket. |
| `assignee_email` | body | `string` | no | Email address belonging to a team member. |
| `status` | body | `string` | no | Status for the ticket. |
| `priority` | body | `string` | no | Priority for the ticket. |
| `category` | body | `string` | no | Category for the ticket. |
| `tags[]` | body | `array<string>` | no | Tags to assign to the ticket. |
