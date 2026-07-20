# List Mailboxes with Salesforge

Retrieves mailboxes from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/mailboxes`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [List Mailboxes](https://api.salesforge.ai/public/v2/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes |
| `statuses[]` | query | `array<string>` | no |
| `mailbox_ids[]` | query | `array<string>` | no |
| `excluded_mailbox_ids[]` | query | `array<string>` | no |
| `search` | query | `string` | no |
| `tag_ids[]` | query | `array<string>` | no |
| `not_tag_ids[]` | query | `array<string>` | no |
| `addresses[]` | query | `array<string>` | no |
| `status_criteria` | query | `string` | no |
| `statuses_criteria[]` | query | `array<string>` | no |
