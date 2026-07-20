# Mark Notification Read/Unread with SeaTable

Marks a SeaTable notification as read or unread.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/notifications/:notification_id/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Mark Notification Read/Unread](https://api.seatable.com/reference/markbasenotificationasseen-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notification_id` | path | `string` | yes | The SeaTable notification ID. |
