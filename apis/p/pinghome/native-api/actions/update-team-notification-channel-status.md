# Update Team Notification Channel Status with Pinghome

Updates team notification channel status in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer-cmd/v1/team/:id/notification-channel/enabled`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Team Notification Channel Status](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/update-team-notification-channel-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the team. |
| `enabled` | body | `boolean` | yes | Boolean value indicating whether the notification channel is enabled or disabled. |
| `priority` | body | `number` | yes | The priority number of the notification channel to update. |
