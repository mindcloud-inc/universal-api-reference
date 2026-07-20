# Mark Notifications As Read with Discourse

Marks current Discourse notifications as read.

## Endpoint

- **Method:** `PUT`
- **Path:** `/notifications/mark-read.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Mark Notifications As Read](https://docs.discourse.org/#tag/Notifications/operation/markNotificationsAsRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | no | Optional notification id. Leave blank to mark all notifications as read. |
