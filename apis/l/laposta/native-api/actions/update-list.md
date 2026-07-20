# Update List with Laposta

Updates an existing list in Laposta.

## Endpoint

- **Method:** `POST`
- **Path:** `/list/:listId`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Update List](https://api.laposta.nl/doc/index.en.php#lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | The ID of the list to update. |
| `name` | body | `string` | no | Updated list name. |
| `locked` | body | `boolean` | no | Whether the list is locked. |
| `remarks` | body | `string` | no | Updated list remarks. |
| `subscribe_notification_email` | body | `string` | no | Notification email for subscriptions. |
| `unsubscribe_notification_email` | body | `string` | no | Notification email for unsubscriptions. |
