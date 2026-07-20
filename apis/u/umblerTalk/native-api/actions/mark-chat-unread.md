# Mark Chat Unread with Umbler Talk

Marks a chat as unread in Umbler Talk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/chats/[:id]/unread/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Mark Chat Unread](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The chat ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
