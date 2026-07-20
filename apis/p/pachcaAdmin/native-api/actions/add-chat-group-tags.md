# Add Chat Group Tags with Pachca (Admin)

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/:id/group_tags`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Add Chat Group Tags](https://dev.pachca.com/api/members/add-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_tag_ids[]` | body | `array<number>` | yes | Group tag ids to add to the chat. |
| `id` | path | `number` | yes | Chat id. |
