# List Team Notification Channels with Pinghome

Retrieves team notification channels from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer-query/v1/team/:id/notification-channels`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Team Notification Channels](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/get-team-notification-channels/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the team. |
