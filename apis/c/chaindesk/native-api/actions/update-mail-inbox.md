# Update Mail Inbox with Chaindesk

Updates a mail inbox in Chaindesk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/mail-inboxes/:mailInboxId`
- **Base URL:** `https://app.chaindesk.ai/api`
- **Official documentation:** [Update Mail Inbox](https://docs.chaindesk.ai/api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mailInboxId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `alias` | body | `string` | yes |
