# Update Inbox with Wrangle

## Endpoint

- **Method:** `PUT`
- **Path:** `/inboxes/:inboxId`
- **Base URL:** `https://slack.wrangle.io/api/v1`
- **Official documentation:** [Update Inbox](https://wrangle.apidocumentation.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | yes | The Wrangle inbox ID. |
| `userRoles.NO_ACCESS[]` | body | `array<string>` | no | Slack user IDs to assign the No Access role for this inbox. |
| `userRoles.REQUESTER[]` | body | `array<string>` | no | Slack user IDs to assign the Requester role for this inbox. |
| `userRoles.OBSERVER[]` | body | `array<string>` | no | Slack user IDs to assign the Observer role for this inbox. |
