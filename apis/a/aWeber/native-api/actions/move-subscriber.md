# Move Subscriber with AWeber

Moves a subscriber in AWeber.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/lists/:listId/subscribers/:subscriberId`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Move Subscriber](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers~1{subscriberId}/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `enforce_custom_field_mapping` | body | `boolean` | no |
| `last_followup_message_number_sent` | body | `number` | no |
| `list_link` | body | `string` | yes |
| `listId` | path | `string` | yes |
| `subscriberId` | path | `string` | yes |
