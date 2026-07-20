# Delete Personal Notification Channel with Pinghome

Deletes an existing personal notification channel from Pinghome.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/customer-cmd/v1/customer/:id/notification-channel`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Delete Personal Notification Channel](https://docs.pinghome.io/customer-account-management/account-settings/delete-personal-notification-channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the customer. |
| `priority` | query | `number` | yes | The priority number of the notification channel to delete. |
