# Update Team with SuperSend

Updates an existing team in SuperSend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/{id}`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Update Team](https://docs.supersend.io/docs/team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `name` | body | `string` | no | — |
| `domain` | body | `string` | no | — |
| `logo` | body | `string` | no | — |
| `about` | body | `string` | no | — |
| `meeting_link` | body | `string` | no | — |
| `meeting_link_text` | body | `string` | no | — |
| `auto_placement_testing` | body | `boolean` | no | — |
| `auto_placement_testing_frequency` | body | `number` | no | Allowed values: 7, 14, 30. |
| `notification_email` | body | `string` | no | — |
| `notification_email_preferences` | body | `object` | no | Per-category preferences for which notification types are sent to notification_email. Only provided keys are updated (merge). |
| `notification_email_preferences.errorNotificationsEmail` | body | `boolean` | no | — |
| `notification_email_preferences.successNotificationsEmail` | body | `boolean` | no | — |
| `notification_email_preferences.warmingNotificationsEmail` | body | `boolean` | no | — |
| `notification_email_preferences.newInboxActivityNotificationsEmail` | body | `boolean` | no | — |
| `notification_email_preferences.linkedinInboxActivityNotificationsEmail` | body | `boolean` | no | — |
| `notification_email_preferences.outOfContactsNotificationsEmail` | body | `boolean` | no | — |
| `inbox_auto_tag_settings` | body | `object` | no | — |
| `inbox_auto_tag_settings.auto_tag_bounced` | body | `boolean` | no | — |
| `inbox_auto_tag_settings.auto_tag_opt_out` | body | `boolean` | no | — |
| `inbox_auto_tag_settings.auto_tag_out_of_office` | body | `boolean` | no | — |
| `inbox_super_views[]` | body | `array<object>` | no | — |
| `inbox_super_views[].id` | body | `string` | no | — |
| `inbox_super_views[].name` | body | `string` | no | — |
| `inbox_super_views[].icon` | body | `string` | no | — |
| `inbox_super_views[].filters` | body | `object` | no | — |
| `inbox_super_views[].filters.mood` | body | `string` | no | Allowed values: positive, negative, neutral, needs_review. |
| `inbox_super_views[].filters.statuses[]` | body | `array<string>` | no | — |
| `inbox_super_views[].filters.lastMessageDirection` | body | `string` | no | Allowed values: inbound, outbound. |
| `inbox_super_views[].filters.labels[]` | body | `array<string>` | no | — |
| `inbox_super_views[].visible` | body | `boolean` | no | — |
| `inbox_super_views[].order` | body | `number` | no | Range: 0 to inf. |
