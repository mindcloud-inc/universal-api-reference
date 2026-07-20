# Create Personal Notification Channel with Pinghome

Creates a new personal notification channel in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer-cmd/v1/customer/:id/notification-channel`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Personal Notification Channel](https://docs.pinghome.io/customer-account-management/account-settings/create-personal-notification-channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The customer id that will own the notification channel. |
| `type` | body | `string` | yes | The notification channel type, such as sms or email. |
| `value` | body | `string` | yes | The notification destination, such as an email address or phone number. |
