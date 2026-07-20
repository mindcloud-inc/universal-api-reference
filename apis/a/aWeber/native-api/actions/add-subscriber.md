# Add Subscriber with AWeber

Creates a new subscriber in AWeber.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/lists/:listId/subscribers`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Add Subscriber](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `ad_tracking` | body | `string` | no |
| `custom_fields` | body | `object` | no |
| `email` | body | `string` | yes |
| `ip_address` | body | `string` | no |
| `last_followup_message_number_sent` | body | `number` | no |
| `listId` | path | `string` | yes |
| `misc_notes` | body | `string` | no |
| `name` | body | `string` | no |
| `strict_custom_fields` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
| `update_existing` | body | `string` | no |
