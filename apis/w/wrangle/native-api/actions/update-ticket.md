# Update Ticket with Wrangle

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:ticketId`
- **Base URL:** `https://slack.wrangle.io/api/v1`
- **Official documentation:** [Update Ticket](https://wrangle.apidocumentation.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The Wrangle ticket ID. |
| `assigneeId` | body | `string` | no | The Slack user ID of the ticket assignee. Use null to unassign. |
| `csatScore` | body | `list` | no | The customer satisfaction score for the ticket. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `description` | body | `string` | no | The ticket description. |
| `followers[]` | body | `array<object>` | no | Follower objects to add to the ticket. |
| `formFieldValues[]` | body | `array<object>` | no | Updated form field values for the ticket. |
| `inboxId` | body | `string` | no | Move the ticket to a new inbox. |
| `name` | body | `string` | no | The updated ticket name. |
| `priority` | body | `list` | no | Updated ticket priority. Accepted values: `0`, `1`, `2`, `3`. |
| `status` | body | `list` | no | Updated ticket status. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `tags[]` | body | `array<string>` | no | Updated ticket tags. |
