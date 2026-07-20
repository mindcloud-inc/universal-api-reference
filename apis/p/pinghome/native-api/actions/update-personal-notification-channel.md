# Update Personal Notification Channel with Pinghome

Updates an existing personal notification channel in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer-cmd/v1/customer/:id/notification-channel`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Personal Notification Channel](https://docs.pinghome.io/customer-account-management/account-settings/update-personal-notification-channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the customer. |
| `value` | body | `string` | yes | The updated notification channel value, such as a phone number or email address. |
| `priority` | body | `number` | yes | The priority number of the notification channel to update. |
