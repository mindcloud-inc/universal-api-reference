# Update Subscriber By ID with AWeber

Updates an existing subscriber in AWeber.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/lists/:listId/subscribers/:subscriberId`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Update Subscriber By ID](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers~1{subscriberId}/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `ad_tracking` | body | `string` | no |
| `custom_fields` | body | `object` | no |
| `email` | body | `string` | no |
| `last_followup_message_number_sent` | body | `number` | no |
| `listId` | path | `string` | yes |
| `misc_notes` | body | `string` | no |
| `name` | body | `string` | no |
| `status` | body | `string` | no |
| `strict_custom_fields` | body | `string` | no |
| `subscriberId` | path | `string` | yes |
| `tags` | body | `object` | no |
| `tags.add[]` | body | `array<string>` | no |
| `tags.remove[]` | body | `array<string>` | no |
