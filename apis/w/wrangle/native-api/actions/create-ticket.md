# Create Ticket with Wrangle

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets`
- **Base URL:** `https://slack.wrangle.io/api/v1`
- **Official documentation:** [Create Ticket](https://wrangle.apidocumentation.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the ticket. |
| `inboxId` | body | `string` | yes | The Wrangle inbox ID that will own the ticket. |
| `requesterId` | body | `string` | yes | The Slack user ID of the ticket requester. |
| `description` | body | `string` | no | The ticket description. |
| `priority` | body | `list` | no | Ticket priority. Accepted values: `0`, `1`, `2`, `3`. |
| `tags[]` | body | `array<string>` | no | Tags to assign to the ticket. |
| `formFieldValues[]` | body | `array<object>` | no | Form field values for the ticket intake form. |
