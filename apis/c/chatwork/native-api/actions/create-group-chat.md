# Create Group Chat with Chatwork

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Create Group Chat](https://developer.chatwork.com/reference/post-rooms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the chat. Maximum length: 255. |
| `members_admin_ids` | body | `string` | yes | Comma-separated account IDs for admin members. At least one account ID is required. Send multiple values as a string separated by `,`. |
| `members_member_ids` | body | `string` | no | Comma-separated account IDs for member users. Send multiple values as a string separated by `,`. |
| `members_readonly_ids` | body | `string` | no | Comma-separated account IDs for read-only members. Send multiple values as a string separated by `,`. |
| `description` | body | `string` | no | Summary of the chat. |
| `icon_preset` | body | `list<string>` | no | Chat icon preset. Accepted values: `beer`, `business`, `check`, `document`, `event`, `group`, `heart`, `idea`, `magcup`, `meeting`, `music`, `project`, `security`, `sports`, `star`, `study`, `travel`. |
| `link` | body | `number` | no | Whether to create an invitation link. |
| `link_code` | body | `string` | no | Path segment for the invitation link. Maximum length: 50. |
| `link_need_acceptance` | body | `number` | no | Whether admin approval is required to join through the invitation link. |
