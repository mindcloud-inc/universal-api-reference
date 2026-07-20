# Update Chat Members with Chatwork

## Endpoint

- **Method:** `PUT`
- **Path:** `/rooms/:room_id/members`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Update Chat Members](https://developer.chatwork.com/reference/put-rooms-room_id-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `members_admin_ids` | body | `string` | yes | Comma-separated account IDs for admin members. At least one account ID is required. Send multiple values as a string separated by `,`. |
| `members_member_ids` | body | `string` | no | Comma-separated account IDs for member users. Send multiple values as a string separated by `,`. |
| `members_readonly_ids` | body | `string` | no | Comma-separated account IDs for read-only members. Send multiple values as a string separated by `,`. |
