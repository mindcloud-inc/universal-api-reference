# Delete User Chat Sessions with Alltius

Deletes chat sessions for an Alltius user.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/delete_chat_sessions_for_uid`
- **Base URL:** `https://app.alltius.ai/api/platform`
- **Official documentation:** [Delete User Chat Sessions](https://app.alltius.ai/api/platform/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | — |
| `session_ids` | body | `object` | yes | Provide a JSON array of session IDs. |
