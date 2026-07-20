# Create Team Notification Channel with Pinghome

Creates a new team notification channel in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer-cmd/v1/team/:id/notification-channel`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Team Notification Channel](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/create-team-notification-channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The team id that will own the notification channel. |
| `type` | body | `string` | yes | The notification channel type, such as sms or email. |
| `value` | body | `string` | yes | The notification destination, such as an email address or phone number. |
