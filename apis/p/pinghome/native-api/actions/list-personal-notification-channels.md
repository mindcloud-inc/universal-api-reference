# List Personal Notification Channels with Pinghome

Retrieves personal notification channels from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer-query/v1/customer/:id/notification-channels`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Personal Notification Channels](https://docs.pinghome.io/customer-account-management/account-settings/get-personal-notification-channels/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the customer. |
