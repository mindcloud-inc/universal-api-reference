# Remove Email from Notifications with GatherUp

Deletes a notification email from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/notifications/email/remove`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Remove Email from Notifications](https://app.gatherup.com/api/doc/business/notifications/email/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `email` | body | `string` | yes | Email address. |
| `type` | body | `string` | yes | Notification type. |
