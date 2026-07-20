# Update Ticket with NeetoDesk

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:ticket_id`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Update Ticket](https://apidocs.neetodesk.com/api-reference/tickets/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `string` | yes | Identifier of the ticket. |
| `subject` | body | `string` | no | Updated ticket subject. |
| `description` | body | `string` | no | Updated ticket description. |
| `status` | body | `string` | no | Updated ticket status. |
| `priority` | body | `string` | no | Updated ticket priority. |
| `tags[]` | body | `array<string>` | no | Tags assigned to the ticket. |
