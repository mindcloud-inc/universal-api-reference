# Remove Chat Group Tag with Pachca (Admin)

## Endpoint

- **Method:** `DELETE`
- **Path:** `/chats/:id/group_tags/:tag_id`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Remove Chat Group Tag](https://dev.pachca.com/api/members/remove-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Chat id. |
| `tag_id` | path | `number` | yes | Group tag id to remove. |
