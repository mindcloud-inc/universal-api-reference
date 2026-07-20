# Update Team Notification Channel with Pinghome

Updates an existing team notification channel in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer-cmd/v1/team/:id/notification-channel`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Team Notification Channel](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/update-team-notification-channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the team. |
| `value` | body | `string` | yes | The new notification channel value. |
| `priority` | body | `number` | yes | The priority number of the notification channel to update. |
