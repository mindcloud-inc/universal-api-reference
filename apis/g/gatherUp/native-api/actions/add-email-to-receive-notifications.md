# Add Email to Receive Notifications with GatherUp

Adds a notification email address in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/notifications/email/add`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Add Email to Receive Notifications](https://app.gatherup.com/api/doc/business/notifications/email/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `email` | body | `string` | yes | Email address. |
| `type` | body | `string` | yes | Notification type. |
