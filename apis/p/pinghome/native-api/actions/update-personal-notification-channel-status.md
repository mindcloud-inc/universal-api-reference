# Update Personal Notification Channel Status with Pinghome

Updates personal notification channel status in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer-cmd/v1/customer/:id/notification-channel/enabled`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Personal Notification Channel Status](https://docs.pinghome.io/customer-account-management/account-settings/update-personal-notification-channel-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the customer. |
| `enabled` | body | `boolean` | yes | The status of the notification channel. |
| `priority` | body | `number` | yes | The priority number of the notification channel to update. |
